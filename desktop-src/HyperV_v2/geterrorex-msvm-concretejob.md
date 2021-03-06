---
Description: Retrieves the error objects for the job, if any exist.
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: GetErrorEx method of the Msvm_ConcreteJob class
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- Msvm_ConcreteJob.GetErrorEx
api_type: 
- COM
api_location: 
- vmms.exe
---

# GetErrorEx method of the Msvm\_ConcreteJob class

Retrieves the error objects for the job, if any exist. When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance. However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.

## Syntax


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## Parameters

<dl> <dt>

*Errors* \[out\]
</dt> <dd>

Type: **string\[\]**

If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job. If the operational status of the job is 2 (OK), then **Null** is returned.

</dd> </dl>

## Return value

Type: **uint32**

This method returns one of the following values.

<dl> <dt>

**Completed with No Error** (0)
</dt> <dt>

**Failed** (32768)
</dt> <dt>

**Access Denied** (32769)
</dt> <dt>

**Not Supported** (32770)
</dt> <dt>

**Status is unknown** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Invalid parameter** (32773)
</dt> <dt>

**System is in used** (32774)
</dt> <dt>

**Invalid state for this operation** (32775)
</dt> <dt>

**Incorrect data type** (32776)
</dt> <dt>

**System is not available** (32777)
</dt> <dt>

**Out of memory** (32778)
</dt> </dl>

## Remarks

Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering. For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## Requirements



|                                     |                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                              |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                                    |
| Namespace<br/>                | Root\\Virtualization\\V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## See also

<dl> <dt>

[**Msvm\_ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 


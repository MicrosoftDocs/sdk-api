---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.Query
title: IVssSoftwareSnapshotProvider::Query
author: windows-sdk-content
description: Queries the provider for information about the shadow copies that the provider has completed.
old-location: base\ivsssoftwaresnapshotprovider_query.htm
tech.root: VSS
ms.assetid: bb238acc-7af0-43cf-bc2e-70e255978fb1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,Query method, IVssSoftwareSnapshotProvider.Query, IVssSoftwareSnapshotProvider::Query, Query, Query method, Query method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_query, vsprov/IVssSoftwareSnapshotProvider::Query
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssSoftwareSnapshotProvider.Query
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssSoftwareSnapshotProvider::Query


## -description


Queries the provider for information about the shadow copies that the provider has completed.


## -parameters




### -param QueriedObjectId [in]

Reserved for system use. The value of this parameter must be GUID_NULL.


### -param eQueriedObjectType [in]

Reserved for system use. The value of this parameter must be VSS_OBJECT_NONE.


### -param eReturnedObjectsType [in]

Reserved for system use. The value of this parameter must be VSS_OBJECT_SNAPSHOT.


### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface pointer, 
      which is initialized on return. Callers must release the interface. This parameter is required and cannot be null.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The query operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error. The provider logged the error in the event log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>
 




## -remarks



Calling the <a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">IVssEnumObject::Next</a> method on the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface that is returned though the 
    <i>ppEnum</i>  parameter will return 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures containing a 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure for each shadow copy.




## -see-also




<a href="https://msdn.microsoft.com/5c95f2fb-c132-489c-af48-2ffafad0b41f">IVssSoftwareSnapshotProvider</a>
 

 


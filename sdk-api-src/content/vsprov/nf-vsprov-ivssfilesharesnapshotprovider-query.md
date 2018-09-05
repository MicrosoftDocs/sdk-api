---
UID: NF:vsprov.IVssFileShareSnapshotProvider.Query
title: IVssFileShareSnapshotProvider::Query
author: windows-sdk-content
description: Gets an enumeration of VSS_SNAPSHOT_PROP structures for all file share snapshots that are available to the application server.
old-location: base\ivssfilesharesnapshotprovider_query.htm
old-project: VSS
ms.assetid: 686d2104-f657-4c3b-967b-d6fb9137be17
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssFileShareSnapshotProvider interface [VSS],Query method, IVssFileShareSnapshotProvider.Query, IVssFileShareSnapshotProvider::Query, Query, Query method [VSS], Query method [VSS],IVssFileShareSnapshotProvider interface, base.ivssfilesharesnapshotprovider_query, vsprov/IVssFileShareSnapshotProvider::Query
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VSS_VOLUME_PROTECTION_INFO, *PVSS_VOLUME_PROTECTION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssFileShareSnapshotProvider.Query
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssFileShareSnapshotProvider::Query


## -description



Gets an enumeration of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structures for all file share snapshots  that are available to the application server.  




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



This method is typically called in response to requester generated snapshot query operations.

Calling the <a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">IVssEnumObject::Next</a> method on the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface that is returned though the 
    <i>ppEnum</i>  parameter will return 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures containing a 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure for each shadow copy.




## -see-also




<a href="https://msdn.microsoft.com/1af45503-2f6f-4266-a0d2-ffc74a7be16f">IVssFileShareSnapshotProvider</a>
 

 


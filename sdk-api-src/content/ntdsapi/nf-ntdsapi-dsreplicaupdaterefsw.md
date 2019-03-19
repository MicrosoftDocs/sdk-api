---
UID: NF:ntdsapi.DsReplicaUpdateRefsW
title: DsReplicaUpdateRefsW function (ntdsapi.h)
author: windows-sdk-content
description: Adds or removes a replication reference for a destination from a source naming context.
old-location: ad\dsreplicaupdaterefs.htm
tech.root: ad
ms.assetid: 158c7e73-0e6c-4b71-a87f-2f60f3db91cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DS_REPUPD_ADD_REFERENCE, DS_REPUPD_ASYNCHRONOUS_OPERATION, DS_REPUPD_DELETE_REFERENCE, DS_REPUPD_WRITEABLE, DsReplicaUpdateRefs, DsReplicaUpdateRefs function [Active Directory], DsReplicaUpdateRefsA, DsReplicaUpdateRefsW, _glines_dsreplicaupdaterefs, ad.dsreplicaupdaterefs, ntdsapi/DsReplicaUpdateRefs, ntdsapi/DsReplicaUpdateRefsA, ntdsapi/DsReplicaUpdateRefsW
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaUpdateRefsW (Unicode) and DsReplicaUpdateRefsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaUpdateRefs
 - DsReplicaUpdateRefsA
 - DsReplicaUpdateRefsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsReplicaUpdateRefsW function


## -description


The <b>DsReplicaUpdateRefs</b> function adds or removes a replication reference for a destination from a source naming context.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name of the source naming context.


### -param DsaDest [in]

Pointer to a constant null-terminated string that specifies the transport-specific address of the destination directory system agent.


### -param pUuidDsaDest [in]

Pointer to a <b>UUID</b> value that contains the destination directory system agent.


### -param Options [in]

Contains a set of flags that provide additional data used to process the request. This can be zero or a combination of one or more of the following values.



#### DS_REPUPD_ADD_REFERENCE

A reference to the destination is added to the source server.



#### DS_REPUPD_ASYNCHRONOUS_OPERATION

The operation is performed asynchronously.



#### DS_REPUPD_DELETE_REFERENCE

A reference to the destination is removed from the source server.



#### DS_REPUPD_WRITEABLE

The reference to the replica  added or removed is writable. Otherwise, it is read-only.


##### - Options.DS_REPUPD_ADD_REFERENCE

A reference to the destination is added to the source server.


##### - Options.DS_REPUPD_ASYNCHRONOUS_OPERATION

The operation is performed asynchronously.


##### - Options.DS_REPUPD_DELETE_REFERENCE

A reference to the destination is removed from the source server.


##### - Options.DS_REPUPD_WRITEABLE

The reference to the replica  added or removed is writable. Otherwise, it is read-only.


## -returns



If the function succeeds,  <b>ERROR_SUCCESS</b> is returned.

If the function fails, the return value can be one of the following.




## -remarks



If both <b>DS_REPUPD_ADD_REFERENCE</b> and <b>DS_REPUPD_DELETE_REFERENCE</b> are set in the <i>Options</i> parameter, a reference to the destination is added if one does not already exist on the server. If a reference to the destination already exists, the reference is updated.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>



<a href="https://msdn.microsoft.com/68c767c4-bbb6-477b-8ffb-94f3ae235375">DsReplicaDel</a>



<a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>



<a href="https://msdn.microsoft.com/20c7f96d-f298-4321-a6f5-910c25e418db">DsReplicaSync</a>
 

 


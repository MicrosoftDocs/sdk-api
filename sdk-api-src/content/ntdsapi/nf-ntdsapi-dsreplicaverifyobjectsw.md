---
UID: NF:ntdsapi.DsReplicaVerifyObjectsW
title: DsReplicaVerifyObjectsW function
author: windows-sdk-content
description: Verifies all objects for a naming context with a source.
old-location: ad\dsreplicaverifyobjects.htm
old-project: ad
ms.assetid: d0e139dc-6aaf-47e1-a76f-4e84f17aa7c6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_EXIST_ADVISORY_MODE, DsReplicaVerifyObjects, DsReplicaVerifyObjects function [Active Directory], DsReplicaVerifyObjectsA, DsReplicaVerifyObjectsW, ad.dsreplicaverifyobjects, ntdsapi/DsReplicaVerifyObjects, ntdsapi/DsReplicaVerifyObjectsA, ntdsapi/DsReplicaVerifyObjectsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaVerifyObjectsW (Unicode) and DsReplicaVerifyObjectsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaVerifyObjects
 - DsReplicaVerifyObjectsA
 - DsReplicaVerifyObjectsW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: ADAM
---

# DsReplicaVerifyObjectsW function


## -description


The <b>DsReplicaVerifyObjects</b> function verifies all objects for a naming context with a source.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a>, 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a>, or <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a> function.


### -param NameContext [in]

Pointer to a null-terminated string that contains the distinguished name of the naming context.


### -param pUuidDsaSrc [in]

Pointer to a <b>UUID</b> value that contains the <b>objectGuid</b> of the directory system agent object.


### -param ulOptions [in]

Contains a set of flags that modify the behavior of the function. This can be zero or the following value.



#### DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.


##### - ulOptions.DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error otherwise. Possible error values include the following.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>
 

 


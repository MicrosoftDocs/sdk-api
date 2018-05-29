---
UID: NS:naptypes.tagPrivateData
title: tagPrivateData
author: windows-sdk-content
description: Is used to store and retrieve opaque data blobs.
old-location: nap\privatedata_struct.htm
old-project: NAP
ms.assetid: e2859983-3780-464d-b878-e63d974ba386
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PrivateData, PrivateData structure [NAP], nap.privatedata_struct, naptypes/PrivateData, tagPrivateData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PrivateData
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	PrivateData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagPrivateData structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>PrivateData</b> structure is used to store and retrieve opaque data blobs.


## -struct-fields




### -field size

The size, in bytes,  of  <b>data</b> in the range 0 to <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">maxPrivateDataSize</a>.


### -field data

A pointer to the opaque data blob.


## -remarks



The <b>PrivateData</b> structure is used to store state information for the NapAgent and enforcement clients. It is queried and set by the <a href="https://msdn.microsoft.com/faa91ff5-49f5-4aec-81d7-02ec59274f23">INapSystemHealthValidationRequest</a> and <a href="https://msdn.microsoft.com/96b94995-24b8-47ed-880e-6182d1bfe925">INapEnforcementClientConnection</a> interfaces.




## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 


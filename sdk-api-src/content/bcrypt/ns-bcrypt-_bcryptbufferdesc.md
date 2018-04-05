---
UID: NS:bcrypt._BCryptBufferDesc
title: "_BCryptBufferDesc"
author: windows-driver-content
description: Is used to contain a set of generic CNG buffers.
old-location: security\bcryptbufferdesc.htm
old-project: SecCNG
ms.assetid: 7416d417-4b47-4830-aa20-a674d5270428
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PBCryptBufferDesc, BCRYPTBUFFER_VERSION, BCryptBufferDesc, BCryptBufferDesc structure [Security], PBCryptBufferDesc, PBCryptBufferDesc structure pointer [Security], _BCryptBufferDesc, bcrypt/BCryptBufferDesc, bcrypt/PBCryptBufferDesc, security.bcryptbufferdesc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BCryptBufferDesc, *PBCryptBufferDesc
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	BCryptBufferDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCryptBufferDesc structure


## -description


The <b>BCryptBufferDesc</b> structure is used to contain a set of generic CNG buffers.


## -struct-fields




### -field ulVersion

The version of the structure. This must be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPTBUFFER_VERSION"></a><a id="bcryptbuffer_version"></a><dl>
<dt><b>BCRYPTBUFFER_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The default version number.

</td>
</tr>
</table>
 


### -field cBuffers

The number of elements in the <b>pBuffers</b> array.


### -field pBuffers

The address of an array of <a href="https://msdn.microsoft.com/abfc82f0-ec1c-41fb-8bf4-422a839d50c5">BCryptBuffer</a> structures that contain the buffers. The <b>cBuffers</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/33c3cbf7-6c08-42ed-ac3f-feb71f3a9cbf">BCryptDeriveKey</a>
 

 


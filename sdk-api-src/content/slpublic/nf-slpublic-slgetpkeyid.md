---
UID: NF:slpublic.SLGetPKeyId
title: SLGetPKeyId function
author: windows-sdk-content
description: Gets the registered product key ID associated with the product.
old-location: security\slgetpkeyid.htm
tech.root: SecSLApi
ms.assetid: 6255b66f-d121-47a9-a5a6-eca5483b14dd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SLGetPKeyId, SLGetPKeyId function [Security], security.slgetpkeyid, slpublic/SLGetPKeyId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetPKeyId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SLGetPKeyId function


## -description


Gets the registered product key ID associated with the product.


## -parameters




### -param hSLC [in]

The handle to the current SLC context.


### -param pwszPKeyAlgorithm [in]

The product key algorithm.


### -param pwszPKeyString [in]

The product key string.


### -param cbPKeySpecificData [in]

The size, in bytes, of the product key specific data. If there is no PKey specific data, set <i>cbPKeySpecificData</i> to 0.


### -param pbPKeySpecificData [in]

A pointer to the product key specific data. If there is no PKey specific data, set <i>pbPKeySpecificData</i> to <b>NULL</b>.


### -param pPKeyId [out]

A pointer to the product key ID.


## -returns



If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PKEY_NOT_INSTALLED</b></dt>
<dt>0xC004F014</dt>
</dl>
</td>
<td width="60%">
The product key is not available.

</td>
</tr>
</table>
 




---
UID: NF:propvarutil.PropVariantToVariant
title: PropVariantToVariant function
author: windows-sdk-content
description: Converts the contents of a PROPVARIANT structure to a VARIANT structure.
old-location: properties\PropVariantToVariant.htm
tech.root: properties
ms.assetid: 34907419-47ae-4f8f-8ce6-5f5e9b098488
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PropVariantToVariant, PropVariantToVariant function [Windows Properties], properties.PropVariantToVariant, propvarutil/PropVariantToVariant, shell.PropVariantToVariant, shell_PropVariantToVariant
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PropVariantToVariant
: 
---

# PropVariantToVariant function


## -description


Converts the contents of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure to a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -parameters




### -param pPropVar [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pVar [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure. When this function returns, the <b>VARIANT</b> contains the converted information.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Normally, the data stored in the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is copied to the <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> without a datatype change. However, in the following cases, there is no direct <b>VARIANT</b> support for the datatype, and they are converted as shown.
                
                


<table class="clsStd">
<tr>
<th>Original <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> Type</th>
<th>Stored as <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> Type</th>
</tr>
<tr>
<td>VT_BLOB, VT_STREAM</td>
<td>VT_UNKNOWN. The <b>punkVal</b> member will contain a pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that contains the source data.</td>
</tr>
<tr>
<td>VT_LPSTR, VT_LPWSTR, VT_CLSID</td>
<td>VT_BSTR</td>
</tr>
<tr>
<td>VT_FILETIME</td>
<td>VT_DATE</td>
</tr>
<tr>
<td>VT_VECTOR|x</td>
<td>VT_ARRAY|y</td>
</tr>
</table>
 



The following types cannot be converted with this function.
            
                

<ul>
<li>VT_STORAGE</li>
<li>VT_BLOB_OBJECT</li>
<li>VT_STREAMED_OBJECT</li>
<li>VT_STORED_OBJECT</li>
<li>VT_CF</li>
<li>VT_VECTOR | VT_CF</li>
</ul>



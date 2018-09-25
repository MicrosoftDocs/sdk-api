---
UID: NF:propvarutil.InitPropVariantFromBuffer
title: InitPropVariantFromBuffer function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure using the contents of a buffer.
old-location: properties\InitPropVariantFromBuffer.htm
tech.root: properties
ms.assetid: a6780070-d8de-40f9-8163-e5306e2aa1cc
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: InitPropVariantFromBuffer, InitPropVariantFromBuffer function [Windows Properties], properties.InitPropVariantFromBuffer, propvarutil/InitPropVariantFromBuffer, shell.InitPropVariantFromBuffer, shell_InitPropVariantFromBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
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
 - InitPropVariantFromBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromBuffer function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure using the contents of a buffer.


## -parameters




### -param pv [in]

Type: <b>const void*</b>

Pointer to the buffer.


### -param cb [in]

Type: <b>UINT</b>

The length of the buffer, in bytes.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_UI1 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromBuffer">InitPropVariantFromBuffer</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// void *pv;
// UINT cb;
// Assume variable pv and cb are initialized and valid. pv points to a buffer  
// and cb contains the size of the buffer in bytes.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromBuffer(pv, cb, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI1.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBuffer">InitVariantFromBuffer</a>



<a href="shell.PropVariantToBuffer">PropVariantToBuffer</a>
 

 


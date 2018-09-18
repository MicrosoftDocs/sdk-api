---
UID: NF:propvarutil.VariantToBuffer
title: VariantToBuffer function
author: windows-sdk-content
description: Extracts the contents of a buffer stored in a VARIANT structure of type VT_ARRRAY | VT_UI1.
old-location: properties\VariantToBuffer.htm
tech.root: properties
ms.assetid: 2d310156-c274-4aaf-aee2-ac311a952889
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: VariantToBuffer, VariantToBuffer function [Windows Properties], _shell_VariantToBuffer, properties.VariantToBuffer, propvarutil/VariantToBuffer, shell.VariantToBuffer
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
 - VariantToBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToBuffer function


## -description


Extracts the contents of a buffer stored in a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure of type VT_ARRRAY | VT_UI1.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


### -param pv [out]

Type: <b>VOID*</b>

Pointer to a buffer of length <i>cb</i> bytes. When this function returns, contains the first <i>cb</i> bytes of the extracted buffer value.


### -param cb [in]

Type: <b>UINT</b>

The size of the <i>pv</i> buffer, in bytes. The buffer should be the same size as the data to be extracted, or smaller.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Data successfully extracted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> was not of type VT_ARRRAY | VT_UI1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> buffer value had fewer than <i>cb</i> bytes.

</td>
</tr>
</table>
 




## -remarks



This function is used when the calling application expects a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> to hold a buffer value. The calling application should check that the value has the expected length before it calls this function.

If the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> has type VT_ARRAY | VT_UI1, this function extracts the first <i>cb</i> bytes from the structure and places them in the buffer pointed to by <i>pv</i>.

If the stored value has fewer than <i>cb</i> bytes, then <a href="shell.VariantToBuffer">VariantToBuffer</a> fails and the buffer is not modified.

If the value has more than <i>cb</i> bytes, then <a href="shell.VariantToBuffer">VariantToBuffer</a> succeeds and truncates the value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToBuffer">VariantToBuffer</a> to access a structure that has been stored in a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialized and valid. 
// The application expects var to hold a WIN32_FIND_DATAW structure 
// with sizeof(WIN32_FIND_DATAW) bytes.

HRESULT hr = E_UNEXPECTED;

// Verify that the value length is acceptable before you call VariantToBuffer.
if (VariantGetElementCount(var) == sizeof(WIN32_FIND_DATAW))
{
    WIN32_FIND_DATAW wfd;

    hr = VariantToBuffer(var, &amp;wfd, sizeof(wfd));

    if (SUCCEEDED(hr))
    {
        // wfd is now initialized.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBuffer">InitVariantFromBuffer</a>



<a href="shell.PropVariantToBuffer">PropVariantToBuffer</a>
 

 


---
UID: NF:propvarutil.PropVariantToBuffer
title: PropVariantToBuffer function
author: windows-sdk-content
description: Extracts the buffer value from a PROPVARIANT structure of type VT_VECTOR | VT_UI1 or VT_ARRRAY | VT_UI1.
old-location: properties\PropVariantToBuffer.htm
tech.root: properties
ms.assetid: 8adfc942-ad91-43bb-8d23-8994026666ff
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PropVariantToBuffer, PropVariantToBuffer function [Windows Properties], properties.PropVariantToBuffer, propvarutil/PropVariantToBuffer, shell.PropVariantToBuffer, shell_PropVariantToBuffer
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
 - PropVariantToBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PropVariantToBuffer
: 
---

# PropVariantToBuffer function


## -description


Extracts the buffer value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure of type VT_VECTOR | VT_UI1 or VT_ARRRAY | VT_UI1. 


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pv [out]

Type: <b>VOID*</b>

Pointer to a buffer of length <i>cb</i> bytes. When this function returns, contains the first <i>cb</i> bytes of the extracted buffer value.


### -param cb [in]

Type: <b>UINT</b>

The buffer length, in bytes.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

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
If successful, or an error value otherwise. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>was of the wrong type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>value had fewer than <i>cb</i> bytes.

</td>
</tr>
</table>
 




## -remarks



This function is used in places where the calling application expects a<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>to hold a buffer value. The calling application should check that the value has the expected length before calling this function.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_UI1 or VT_ARRAY | VT_UI1, this function extracts the first <i>cb</i> bytes from the value and places them in the buffer pointed to by <i>pv</i>. If the value has fewer than <i>cb</i> bytes, then <a href="shell.PropVariantToBuffer">PropVariantToBuffer</a> fails and the buffer is not modified. If the value has more than <i>cb</i> bytes, then <b>PropVariantToBuffer</b> succeeds and truncates the value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use PropVariantToBuffer to access a structure that has been stored in a PROPVARIANT".

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_FindData, &amp;propvar);

if (SUCCEEDED(hr))
{
    // PKEY_FindData is expected to produce a VT_VECTOR | VT_UI1 with sizeof(WIN32_FIND_DATAW) bytes
    // We need to verify that the value length is acceptable before calling PropVariantToBuffer
    hr = E_UNEXPECTED;
    
    if (PropVariantGetElementCount(propvar) == sizeof(WIN32_FIND_DATAW))
    {
        WIN32_FIND_DATAW wfd;
        hr = PropVariantToBuffer(propvar, &amp;wfd, sizeof(wfd));
        
        if (SUCCEEDED(hr))
        {
            // wfd is now initialized
        }
    }
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromBuffer">InitPropVariantFromBuffer</a>



<a href="shell.VariantToBuffer">VariantToBuffer</a>
 

 


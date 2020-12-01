---
UID: NF:propvarutil.VariantToBuffer
title: VariantToBuffer function (propvarutil.h)
description: Extracts the contents of a buffer stored in a VARIANT structure of type VT_ARRRAY | VT_UI1.
helpviewer_keywords: ["VariantToBuffer","VariantToBuffer function [Windows Properties]","_shell_VariantToBuffer","properties.VariantToBuffer","propvarutil/VariantToBuffer","shell.VariantToBuffer"]
old-location: properties\VariantToBuffer.htm
tech.root: properties
ms.assetid: 2d310156-c274-4aaf-aee2-ac311a952889
ms.date: 12/05/2018
ms.keywords: VariantToBuffer, VariantToBuffer function [Windows Properties], _shell_VariantToBuffer, properties.VariantToBuffer, propvarutil/VariantToBuffer, shell.VariantToBuffer
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantToBuffer
 - propvarutil/VariantToBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToBuffer
---

# VariantToBuffer function


## -description

Extracts the contents of a buffer stored in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure of type VT_ARRRAY | VT_UI1.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

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
The <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> was not of type VT_ARRRAY | VT_UI1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> buffer value had fewer than <i>cb</i> bytes.

</td>
</tr>
</table>

## -remarks

This function is used when the calling application expects a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to hold a buffer value. The calling application should check that the value has the expected length before it calls this function.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> has type VT_ARRAY | VT_UI1, this function extracts the first <i>cb</i> bytes from the structure and places them in the buffer pointed to by <i>pv</i>.

If the stored value has fewer than <i>cb</i> bytes, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobuffer">VariantToBuffer</a> fails and the buffer is not modified.

If the value has more than <i>cb</i> bytes, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobuffer">VariantToBuffer</a> succeeds and truncates the value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobuffer">VariantToBuffer</a> to access a structure that has been stored in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>.


```cpp
// VARIANT var;
// Assume variable var is initialized and valid. 
// The application expects var to hold a WIN32_FIND_DATAW structure 
// with sizeof(WIN32_FIND_DATAW) bytes.

HRESULT hr = E_UNEXPECTED;

// Verify that the value length is acceptable before you call VariantToBuffer.
if (VariantGetElementCount(var) == sizeof(WIN32_FIND_DATAW))
{
    WIN32_FIND_DATAW wfd;

    hr = VariantToBuffer(var, &wfd, sizeof(wfd));

    if (SUCCEEDED(hr))
    {
        // wfd is now initialized.
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfrombuffer">InitVariantFromBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobuffer">PropVariantToBuffer</a>
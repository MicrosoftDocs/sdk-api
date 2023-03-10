---
UID: NF:adshlp.ADsEncodeBinaryData
title: ADsEncodeBinaryData function (adshlp.h)
description: The ADsEncodeBinaryData function converts a binary large object (BLOB) to the Unicode format suitable to be embedded in a search filter.
helpviewer_keywords: ["ADsEncodeBinaryData","ADsEncodeBinaryData function [ADSI]","_ds_adsencodebinarydata","adshlp/ADsEncodeBinaryData","adsi.adsencodebinarydata"]
old-location: adsi\adsencodebinarydata.htm
tech.root: adsi
ms.assetid: b7bdf16c-7533-4db6-9bc4-06bc57d864ec
ms.date: 12/05/2018
ms.keywords: ADsEncodeBinaryData, ADsEncodeBinaryData function [ADSI], _ds_adsencodebinarydata, adshlp/ADsEncodeBinaryData, adsi.adsencodebinarydata
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll; AdsLdpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsEncodeBinaryData
 - adshlp/ADsEncodeBinaryData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
 - AdsLdpc.dll
api_name:
 - ADsEncodeBinaryData
---

# ADsEncodeBinaryData function


## -description

The <b>ADsEncodeBinaryData</b> function converts a binary large object (BLOB) to the Unicode format suitable to be embedded in a search filter.

## -parameters

### -param pbSrcData [in]

Type: <b>PBYTE</b>

BLOB to be converted.

### -param dwSrcLen [in]

Type: <b>DWORD</b>

Size, in bytes, of the BLOB.

### -param ppszDestData [out]

Type: <b>LPWSTR*</b>

Pointer to a null-terminated Unicode string that receives the converted data.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values, as well as the following.

## -remarks

In ADSI, search filters must be Unicode strings. Sometimes, a filter contains data that is normally represented by an opaque BLOB of data. For example, you may want to include an object security identifier in a search filter, which is of binary data. In this case, you must first call the <b>ADsEncodeBinaryData</b> function to convert the binary data to the Unicode string format. When the data is no longer required, call the  <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> function to free the converted Unicode string; that is, <i>ppszDestData</i>.

The <b>ADsEncodeBinaryData</b> function does not encode byte values that represent alpha-numeric characters. It will, instead, place the character into the string without encoding it. This results in the string containing a mixture of encoded and unencoded characters. For example, if the binary data is 0x05|0x1A|0x1B|0x43|0x32, the encoded string will contain "\05\1A\1BC2". This has no effect on the filter and the search filters will work correctly with these types of strings.


#### Examples

The following code example shows how to use this function.


```cpp
// Test binary values in filters and use
// a binary filter instead of a string filter in ExecuteSearch.

LPWSTR pszPrefix = L"objectSid=%s";
LPWSTR pszBinaryFilter = NULL;
LPWSTR pszDest = NULL;
HRESULT hr = S_OK;
 
BYTE column[] = {
  0x01, 0x05, 0x00, 0x00, 0x00, 0x00, 0x00, 0x05, 0x15, 0x00,
  0x00, 0x00, 0x59, 0x51, 0xb8, 0x17, 0x66, 0x72, 0x5d, 0x25,
  0x64, 0x63, 0x3b, 0x0b, 0x29, 0x99, 0x21, 0x00 };

DWORD dwSize = sizeof(column)/sizeof(BYTE);
 
hr = ADsEncodeBinaryData (
    column,
    dwSize,
    &pszDest
    );

if(hr==S_OK)
{
    dwSize = wcslen(pszPrefix) + wcslen(pszDest) + 1;
    pszBinaryFilter = new WCHAR[dwSize];
    sprintf_s(pszBinaryFilter,pszPrefix,pszDest);
}
else
{
    return hr;
}


 
// Perform the search with the pszDest as the filter string. Code omitted.
. . . 
// Done with the search and free the converted string.
FreeADsMem( pszDest );
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>
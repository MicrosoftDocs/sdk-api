---
UID: NF:propsys.PSStringFromPropertyKey
title: PSStringFromPropertyKey function (propsys.h)
description: Creates a string that identifies a property from that property's key.
helpviewer_keywords: ["PSStringFromPropertyKey","PSStringFromPropertyKey function [Windows Properties]","_shell_PSStringFromPropertyKey","properties.PSStringFromPropertyKey","propsys/PSStringFromPropertyKey","shell.PSStringFromPropertyKey"]
old-location: properties\PSStringFromPropertyKey.htm
tech.root: properties
ms.assetid: 081f8e6d-9189-44f9-9b27-e85f4793da48
ms.date: 12/05/2018
ms.keywords: PSStringFromPropertyKey, PSStringFromPropertyKey function [Windows Properties], _shell_PSStringFromPropertyKey, properties.PSStringFromPropertyKey, propsys/PSStringFromPropertyKey, shell.PSStringFromPropertyKey
req.header: propsys.h
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
 - PSStringFromPropertyKey
 - propsys/PSStringFromPropertyKey
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
 - PSStringFromPropertyKey
---

# PSStringFromPropertyKey function


## -description

Creates a string that identifies a property from that property's key.

## -parameters

### -param pkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that identifies a property.

### -param psz [out]

Type: <b>LPWSTR</b>

Pointer to a buffer that receives the output string. The buffer should be large enough to contain PKEYSTR_MAX <b>WCHAR</b><b>s</b>.

### -param cch [in]

Type: <b>UINT</b>

The length of the buffer pointed to by <i>psz</i>, in <b>WCHAR</b><b>s</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string format retrieved is <code>"{propkey.fmtid} propkey.pid"</code>. For example, the output string for <code>PKEY_Title</code> is <code>"{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 2"</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates the use of <a href="/windows/desktop/api/propsys/nf-propsys-pspropertykeyfromstring">PSPropertyKeyFromString</a>.


```cpp
WCHAR szKey[PKEYSTR_MAX]

HRESULT hr = PSStringFromPropertyKey(PKEY_Title, szKey, ARRAYSIZE(szKey));

if (SUCCEEDED(hr))
{
    // szKey is now valid.
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psgetnamefrompropertykey">PSGetNameFromPropertyKey</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pspropertykeyfromstring">PSPropertyKeyFromString</a>
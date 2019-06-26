---
UID: NF:propvarutil.PropVariantToGUID
title: PropVariantToGUID function (propvarutil.h)
author: windows-sdk-content
description: Extracts a GUID value from a PROPVARIANT structure.
old-location: properties\PropVariantToGUID.htm
tech.root: properties
ms.assetid: cf1d884b-41d4-429a-afb7-c66c67526796
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropVariantToGUID, PropVariantToGUID function [Windows Properties], properties.PropVariantToGUID, propvarutil/PropVariantToGUID, shell.PropVariantToGUID, shell_PropVariantToGUID
ms.topic: function
f1_keywords: 
 - "propvarutil/PropVariantToGUID"
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
 - PropVariantToGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantToGUID function


## -description


Extracts a GUID value from a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.


### -param pguid [out]

Type: <b>GUID*</b>

When this function returns, contains the extracted property value if one exists.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>structures of the following types: 
          

<ul>
<li>VT_GUID</li>
<li>VT_BSTR</li>
<li>VT_LPWSTR</li>
<li>VT_ARRAY | VT_UI1</li>
</ul>

<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoguid">PropVariantToGUID</a> is used in places where the calling application expects a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> to hold a single <b>GUID</b> or <b>GUID</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>GUID</b> value for <b>GUID</b> properties.


#### Examples


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Sync_HandlerCollectionID, &propvar);

if (SUCCEEDED(hr))

{

        // PKEY_Sync_HandlerCollectionID is expected to produce a VT_CLSID or VT_EMPTY value.

        // PropVariantToGUID will convert VT_EMPTY to a failure code.

        GUID guidCollectionID;

        hr = PropVariantToGUID(propvar, &guidCollectionID);

        if (SUCCEEDED(hr))

        {

             // guidCollectionID is now valid

        }

        else

        {

            // the extraction failed

        }

        PropVariantClear(&propvar);

}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromclsid">InitPropVariantFromCLSID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoclsid">PropVariantToCLSID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttoguid">VariantToGUID</a>
 

 


---
UID: NF:propvarutil.PropVariantToGUID
title: PropVariantToGUID function
author: windows-driver-content
description: Extracts a GUID value from a PROPVARIANT structure.
old-location: properties\PropVariantToGUID.htm
old-project: properties
ms.assetid: cf1d884b-41d4-429a-afb7-c66c67526796
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PropVariantToGUID, PropVariantToGUID function [Windows Properties], properties.PropVariantToGUID, propvarutil/PropVariantToGUID, shell.PropVariantToGUID, shell_PropVariantToGUID
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantToGUID
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PropVariantToGUID function


## -description


Extracts a GUID value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar

TBD


### -param pguid [out]

Type: <b>GUID*</b>

When this function returns, contains the extracted property value if one exists.


#### - propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>structures of the following types: 
          

<ul>
<li>VT_GUID</li>
<li>VT_BSTR</li>
<li>VT_LPWSTR</li>
<li>VT_ARRAY | VT_UI1</li>
</ul>

<a href="shell.PropVariantToGUID">PropVariantToGUID</a> is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a single <b>GUID</b> or <b>GUID</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>GUID</b> value for <b>GUID</b> properties.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_Sync_HandlerCollectionID, &amp;propvar);

if (SUCCEEDED(hr))

{

        // PKEY_Sync_HandlerCollectionID is expected to produce a VT_CLSID or VT_EMPTY value.

        // PropVariantToGUID will convert VT_EMPTY to a failure code.

        GUID guidCollectionID;

        hr = PropVariantToGUID(propvar, &amp;guidCollectionID);

        if (SUCCEEDED(hr))

        {

             // guidCollectionID is now valid

        }

        else

        {

            // the extraction failed

        }

        PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromCLSID">InitPropVariantFromCLSID</a>



<a href="shell.PropVariantToCLSID">PropVariantToCLSID</a>



<a href="shell.VariantToGUID">VariantToGUID</a>
 

 


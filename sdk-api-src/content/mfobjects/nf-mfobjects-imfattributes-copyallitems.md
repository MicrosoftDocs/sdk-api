---
UID: NF:mfobjects.IMFAttributes.CopyAllItems
title: IMFAttributes::CopyAllItems (mfobjects.h)
description: Copies all of the attributes from this object into another attribute store.
helpviewer_keywords: ["111b55bc-fb8e-45b5-a709-703acd23c4be","CopyAllItems","CopyAllItems method [Media Foundation]","CopyAllItems method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","CopyAllItems method","IMFAttributes.CopyAllItems","IMFAttributes::CopyAllItems","mf.imfattributes_copyallitems","mfobjects/IMFAttributes::CopyAllItems"]
old-location: mf\imfattributes_copyallitems.htm
tech.root: mf
ms.assetid: 111b55bc-fb8e-45b5-a709-703acd23c4be
ms.date: 12/05/2018
ms.keywords: 111b55bc-fb8e-45b5-a709-703acd23c4be, CopyAllItems, CopyAllItems method [Media Foundation], CopyAllItems method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],CopyAllItems method, IMFAttributes.CopyAllItems, IMFAttributes::CopyAllItems, mf.imfattributes_copyallitems, mfobjects/IMFAttributes::CopyAllItems
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAttributes::CopyAllItems
 - mfobjects/IMFAttributes::CopyAllItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.CopyAllItems
---

# IMFAttributes::CopyAllItems


## -description

Copies all of the attributes from this object into another attribute store.

## -parameters

### -param pDest [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store that receives the copy.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method deletes all of the attributes originally stored in <i>pDest</i>.
      

<div class="alert"><b>Note</b>  <p class="note">When you call <b>CopyAllItems</b> on an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>, which inherits this method, the sample time, duration, and flags are not copied to the destination sample. You must copy these values to the new sample manually.

</div>
<div> </div>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

To copy a single attribute rather than all of the attributes, you can use the following code:


```cpp
HRESULT CopyAttribute(IMFAttributes *pFrom, IMFAttributes *pTo, REFGUID guidKey)
{
    PROPVARIANT val;

    HRESULT hr = pFrom->GetItem(guidKey, &val);

    if (SUCCEEDED(hr))
    {
        hr = pTo->SetItem(guidKey, val);
        PropVariantClear(&val);
    }
    else if (hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = S_OK;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
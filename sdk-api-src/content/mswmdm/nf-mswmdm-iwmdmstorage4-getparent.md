---
UID: NF:mswmdm.IWMDMStorage4.GetParent
title: IWMDMStorage4::GetParent (mswmdm.h)
description: The GetParent method retrieves the parent of the storage.
helpviewer_keywords: ["GetParent","GetParent method [windows Media Device Manager]","GetParent method [windows Media Device Manager]","IWMDMStorage4 interface","IWMDMStorage4 interface [windows Media Device Manager]","GetParent method","IWMDMStorage4.GetParent","IWMDMStorage4::GetParent","IWMDMStorage4GetParent","mswmdm/IWMDMStorage4::GetParent","wmdm.iwmdmstorage4_getparent"]
old-location: wmdm\iwmdmstorage4_getparent.htm
tech.root: WMDM
ms.assetid: e3281501-ec4b-4437-b462-d5b0fd1ac4e0
ms.date: 12/05/2018
ms.keywords: GetParent, GetParent method [windows Media Device Manager], GetParent method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetParent method, IWMDMStorage4.GetParent, IWMDMStorage4::GetParent, IWMDMStorage4GetParent, mswmdm/IWMDMStorage4::GetParent, wmdm.iwmdmstorage4_getparent
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMStorage4::GetParent
 - mswmdm/IWMDMStorage4::GetParent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage4.GetParent
---

# IWMDMStorage4::GetParent


## -description

The <b>GetParent</b> method retrieves the parent of the storage.

## -parameters

### -param ppStorage [out]

Pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a> interface of the parent storage. The caller must release this interface when finished with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The application can navigate up the storage hierarchy by calling <b>GetParent</b> recursively. After the root storage is reached, <b>GetParent</b> returns S_FALSE and sets <i>ppStorage</i> to <b>NULL</b>.


#### Examples

The following C++ function traverses up to the root parent of a storage.


```cpp

HRESULT BubbleUp(IWMDMStorage *pIStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage4> pStorage4;

    hr = pIStorage->QueryInterface (__uuidof(IWMDMStorage4), reinterpret_cast<void**>(&pStorage4));
    if (SUCCEEDED(hr))
    {
        while ((pStorage4 != NULL))
        {
            CComPtr<IWMDMStorage> pParent;
            hr = pStorage4->GetParent(&pParent);
            if (FAILED(hr))
            {
                break;
            }

            //
            // Do something with pParent....
            //
            
            if (S_FALSE != hr)
            {
                hr = pParent->QueryInterface (__uuidof(IMDSPStorage4), reinterpret_cast<void**>(&pStorage4));
                if (FAILED(hr))
                {
                    break;
                }
            }
        } // Loop up to next parent.
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>
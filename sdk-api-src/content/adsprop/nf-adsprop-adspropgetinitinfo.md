---
UID: NF:adsprop.ADsPropGetInitInfo
title: ADsPropGetInitInfo function (adsprop.h)
description: Used to obtain directory object data that an Active Directory Domain Services property sheet extension applies to.
helpviewer_keywords: ["ADsPropGetInitInfo","ADsPropGetInitInfo function [Active Directory]","ad.adspropgetinitinfo","adsprop/ADsPropGetInitInfo"]
old-location: ad\adspropgetinitinfo.htm
tech.root: ad
ms.assetid: dcc4ea8f-6924-4e26-a675-ce326f35933c
ms.date: 12/05/2018
ms.keywords: ADsPropGetInitInfo, ADsPropGetInitInfo function [Active Directory], ad.adspropgetinitinfo, adsprop/ADsPropGetInitInfo
req.header: adsprop.h
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
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsPropGetInitInfo
 - adsprop/ADsPropGetInitInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsprop.dll
api_name:
 - ADsPropGetInitInfo
---

# ADsPropGetInitInfo function


## -description

The <b>ADsPropGetInitInfo</b> function is used to obtain directory object data that an Active Directory Domain Services property sheet extension applies to.

## -parameters

### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>.

### -param pInitParams [out]

Pointer to an <a href="/windows/desktop/api/adsprop/ns-adsprop-adspropinitparams">ADSPROPINITPARAMS</a> structure that receives the directory object data. The <b>dwSize</b> member of this structure must be entered before calling this function.

## -returns

Returns nonzero if successful or zero otherwise.

## -remarks

The memory  for the <b>pwzCN</b> and <b>pWritableAttrs</b> members is allocated by the <b>ADsPropGetInitInfo</b> function. This memory is freed by the system after all property sheet objects are destroyed. The reference count for the interface pointer in <b>pDsObj</b> is not incremented by calling <b>ADsPropGetInitInfo</b>, so the interface must not be released by the caller.

For multiple-selection property sheets, the system only binds to the first object in the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsobject">DSOBJECT</a> array. Because of this, <b>ADsPropGetInitInfo</b> only supplies the <a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a> and writable attributes for the first object in the array. The other objects in the array are not bound to.


#### Examples

The following code example shows how to use the <b>ADsPropGetInitInfo</b> function.


```cpp
HRESULT GetADsPageInfo(HWND hwndNotifyObject, ADSPROPINITPARAMS *pip)
{
    if((NULL == pip) || (!IsWindow(hwndNotifyObject)))
    {
        return E_INVALIDARG;
    }

    ADSPROPINITPARAMS   InitParams;
    
    InitParams.dwSize = sizeof(ADSPROPINITPARAMS);
    if(ADsPropGetInitInfo(hwndNotifyObject, &InitParams))
    {
        *pip = InitParams;
    
        return InitParams.hr;
    }
    
    return E_FAIL;
}

```

## -see-also

<a href="/windows/desktop/api/adsprop/ns-adsprop-adspropinitparams">ADSPROPINITPARAMS</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>
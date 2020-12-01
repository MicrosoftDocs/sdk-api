---
UID: NF:adsprop.ADsPropCreateNotifyObj
title: ADsPropCreateNotifyObj function (adsprop.h)
description: The ADsPropCreateNotifyObj function is used to create, or obtain, a notification object for use by an Active Directory Domain Services property sheet extension.
helpviewer_keywords: ["ADsPropCreateNotifyObj","ADsPropCreateNotifyObj function [Active Directory]","ad.adspropcreatenotifyobj","adsprop/ADsPropCreateNotifyObj"]
old-location: ad\adspropcreatenotifyobj.htm
tech.root: ad
ms.assetid: bfca3801-0d24-4177-8173-b6bf4b854fae
ms.date: 12/05/2018
ms.keywords: ADsPropCreateNotifyObj, ADsPropCreateNotifyObj function [Active Directory], ad.adspropcreatenotifyobj, adsprop/ADsPropCreateNotifyObj
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
 - ADsPropCreateNotifyObj
 - adsprop/ADsPropCreateNotifyObj
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
 - ADsPropCreateNotifyObj
---

# ADsPropCreateNotifyObj function


## -description

The <b>ADsPropCreateNotifyObj</b> function is used to create, or obtain, a notification object for use by an Active Directory Domain Services property sheet extension.

## -parameters

### -param pAppThdDataObj [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object that represents the directory object that the property page applies to. This is the <b>IDataObject</b> passed to the property page <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize">IShellExtInit::Initialize</a> method.

### -param pwzADsObjName [in]

The Active Directory Domain Services object name obtained by calling the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method for the <a href="/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format">CFSTR_DSOBJECTNAMES</a> clipboard format on the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> represented by <i>pAppThdDataObj</i>.

### -param phNotifyObj [out]

Pointer to an <b>HWND</b> value that receives the handle of the notification object.

## -returns

Returns <b>S_OK</b> if successful, or an OLE-defined error value otherwise.

## -remarks

The <b>ADsPropCreateNotifyObj</b> function is used in the implementation of an Active Directory Domain Services property sheet extension. The extension must first request the  <a href="/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format">CFSTR_DSOBJECTNAMES</a> data from the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize">IShellExtInit::Initialize</a> by calling <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. This provides the data object and object name required to call <b>ADsPropCreateNotifyObj</b>.

When the notification object is no longer required, a <a href="/windows/desktop/AD/wm-adsprop-notify-exit">WM_ADSPROP_NOTIFY_EXIT</a> message is sent to the notification object. This causes the notification object to destroy itself. When the <b>WM_ADSPROP_NOTIFY_EXIT</b> message is sent, the notification object handle should be considered invalid.


#### Examples

The following C++ example shows how to use the <b>ADsPropCreateNotifyObj</b> function.


```cpp
HWND CreateADsNotificationObject(IDataObject *pDataObject)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;
    HWND        hwndNotifyObject = NULL;

    if(NULL == pDataObject)
    {
        return NULL;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    if(0 == fe.cfFormat)
    {
        return NULL;
    }
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObject->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = 
            (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            LPWSTR  pwszName = (LPWSTR)((LPBYTE)pdson + 
                pdson->aObjects[0].offsetName);
            
            hr = ADsPropCreateNotifyObj(pDataObject, 
                pwszName, 
                &hwndNotifyObject);
    
            GlobalUnlock(stm.hGlobal);    
        }
        
        ReleaseStgMedium(&stm);
    }

    return hwndNotifyObject;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format">CFSTR_DSOBJECTNAMES</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a>



<a href="/windows/desktop/AD/wm-adsprop-notify-exit">WM_ADSPROP_NOTIFY_EXIT</a>
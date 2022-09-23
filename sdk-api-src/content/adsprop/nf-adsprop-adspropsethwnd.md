---
UID: NF:adsprop.ADsPropSetHwnd
title: ADsPropSetHwnd function (adsprop.h)
description: Used to notify the notification object of the property page window handle. (ADsPropSetHwnd)
helpviewer_keywords: ["ADsPropSetHwnd","ADsPropSetHwnd function [Active Directory]","_glines_adspropsethwnd","ad.adspropsethwnd","adsprop/ADsPropSetHwnd"]
old-location: ad\adspropsethwnd.htm
tech.root: ad
ms.assetid: 9fc6b86b-e075-4969-842c-3ebddd43db8f
ms.date: 12/05/2018
ms.keywords: ADsPropSetHwnd, ADsPropSetHwnd function [Active Directory], _glines_adspropsethwnd, ad.adspropsethwnd, adsprop/ADsPropSetHwnd
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
 - ADsPropSetHwnd
 - adsprop/ADsPropSetHwnd
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
 - ADsPropSetHwnd
---

# ADsPropSetHwnd function


## -description

The <b>ADsPropSetHwnd</b> function is used to notify the notification object of the property page window handle.

## -parameters

### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>.

### -param hPage [in]

A window handle of the property page.

## -returns

Returns zero if the notification object does not exist or nonzero otherwise.

## -remarks

An Active Directory Domain Services property sheet extension normally calls this function while processing the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

If the property sheet extension uses the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a> function, the extension should use <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsethwndwithtitle">ADsPropSetHwndWithTitle</a> rather than <b>ADsPropSetHwnd</b>.

## -see-also

<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsethwndwithtitle">ADsPropSetHwndWithTitle</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>

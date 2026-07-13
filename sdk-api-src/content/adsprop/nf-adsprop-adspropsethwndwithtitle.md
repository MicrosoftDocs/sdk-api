---
UID: NF:adsprop.ADsPropSetHwndWithTitle
title: ADsPropSetHwndWithTitle function (adsprop.h)
description: Used to notify the notification object of the property page window handle. (ADsPropSetHwndWithTitle)
helpviewer_keywords: ["ADsPropSetHwndWithTitle","ADsPropSetHwndWithTitle function [Active Directory]","ad.adspropsethwndwithtitle","adsprop/ADsPropSetHwndWithTitle"]
old-location: ad\adspropsethwndwithtitle.htm
tech.root: ad
ms.assetid: d0d26f32-1c15-4641-bdeb-0f464a510669
ms.date: 12/05/2018
ms.keywords: ADsPropSetHwndWithTitle, ADsPropSetHwndWithTitle function [Active Directory], ad.adspropsethwndwithtitle, adsprop/ADsPropSetHwndWithTitle
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
 - ADsPropSetHwndWithTitle
 - adsprop/ADsPropSetHwndWithTitle
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
 - ADsPropSetHwndWithTitle
---

# ADsPropSetHwndWithTitle function


## -description

The <b>ADsPropSetHwndWithTitle</b> function is used to notify the notification object of the property page window handle.This function includes the title of the property page which enables the error dialog displayed by <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a> to provide more useful information to the user.

## -parameters

### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>.

### -param hPage [in]

A window handle of the property page.

### -param ptzTitle [in]

Pointer to a NULL-terminated string that contains the property page title.

## -returns

Returns zero if the notification object does not exist or nonzero otherwise.

## -remarks

An Active Directory Domain Services property sheet extension normally calls this function while processing the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

If the property sheet extension uses the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a> function, the extension should use <b>ADsPropSetHwndWithTitle</b> rather than <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsethwnd">ADsPropSetHwnd</a>.

## -see-also

<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsethwnd">ADsPropSetHwnd</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>

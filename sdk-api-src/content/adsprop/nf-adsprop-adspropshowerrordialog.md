---
UID: NF:adsprop.ADsPropShowErrorDialog
title: ADsPropShowErrorDialog function (adsprop.h)
description: The ADsPropShowErrorDialog function displays a dialog box that contains the error messages accumulated through calls to the ADsPropSendErrorMessage function or the WM_ADSPROP_NOTIFY_ERROR.
helpviewer_keywords: ["ADsPropShowErrorDialog","ADsPropShowErrorDialog function [Active Directory]","ad.adspropshowerrordialog","adsprop/ADsPropShowErrorDialog"]
old-location: ad\adspropshowerrordialog.htm
tech.root: ad
ms.assetid: c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83
ms.date: 12/05/2018
ms.keywords: ADsPropShowErrorDialog, ADsPropShowErrorDialog function [Active Directory], ad.adspropshowerrordialog, adsprop/ADsPropShowErrorDialog
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
 - ADsPropShowErrorDialog
 - adsprop/ADsPropShowErrorDialog
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
 - ADsPropShowErrorDialog
---

# ADsPropShowErrorDialog function


## -description

The <b>ADsPropShowErrorDialog</b> function displays a dialog box that contains the error messages accumulated through calls to the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsenderrormessage">ADsPropSendErrorMessage</a> function or the <a href="/windows/desktop/AD/wm-adsprop-notify-error">WM_ADSPROP_NOTIFY_ERROR</a>.

## -parameters

### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>.

### -param hPage [in]

The window handle of the property page.

## -returns

Returns zero if the notification object does not exist or nonzero otherwise.

## -remarks

The error messages added by the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsenderrormessage">ADsPropSendErrorMessage</a> function are accumulated until  <b>ADsPropShowErrorDialog</b> is called.  <b>ADsPropShowErrorDialog</b> combines and displays the accumulated  error messages. When the error dialog is dismissed, the accumulated error messages are deleted.

## -see-also

<a href="/windows/desktop/api/adsprop/ns-adsprop-adsproperror">ADSPROPERROR</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsenderrormessage">ADsPropSendErrorMessage</a>



<a href="/windows/desktop/AD/messages-in-active-directory-domain-services">Messages in Active Directory Domain Services</a>



<a href="/windows/desktop/AD/wm-adsprop-notify-error">WM_ADSPROP_NOTIFY_ERROR</a>
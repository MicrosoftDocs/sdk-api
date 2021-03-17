---
UID: NF:adsprop.ADsPropSendErrorMessage
title: ADsPropSendErrorMessage function (adsprop.h)
description: The ADsPropSendErrorMessage function adds an error message to a list of error messages displayed by calling the ADsPropShowErrorDialog function.
helpviewer_keywords: ["ADsPropSendErrorMessage","ADsPropSendErrorMessage function [Active Directory]","ad.adspropsenderrormessage","adsprop/ADsPropSendErrorMessage"]
old-location: ad\adspropsenderrormessage.htm
tech.root: ad
ms.assetid: a1ca8440-0b18-4439-9143-bd8119f4f6ae
ms.date: 12/05/2018
ms.keywords: ADsPropSendErrorMessage, ADsPropSendErrorMessage function [Active Directory], ad.adspropsenderrormessage, adsprop/ADsPropSendErrorMessage
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
 - ADsPropSendErrorMessage
 - adsprop/ADsPropSendErrorMessage
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
 - ADsPropSendErrorMessage
---

# ADsPropSendErrorMessage function


## -description

The <b>ADsPropSendErrorMessage</b> function adds an error message to a list of error messages displayed by calling 
the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a> function.

## -parameters

### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropcreatenotifyobj">ADsPropCreateNotifyObj</a>.

### -param pError [out]

Pointer to an <a href="/windows/desktop/api/adsprop/ns-adsprop-adsproperror">ADSPROPERROR</a> structure which contains data about the error message.

## -returns

Returns nonzero if successful or zero otherwise.

## -remarks

The error messages added by the <b>ADsPropSendErrorMessage</b> function are accumulated until  <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a> is called.  <b>ADsPropShowErrorDialog</b> combines and displays the accumulated  error messages. When the error dialog is dismissed, the accumulated error messages are deleted.

## -see-also

<a href="/windows/desktop/api/adsprop/ns-adsprop-adsproperror">ADSPROPERROR</a>



<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropshowerrordialog">ADsPropShowErrorDialog</a>



<a href="/windows/desktop/AD/messages-in-active-directory-domain-services">Messages in Active Directory Domain Services</a>



<a href="/windows/desktop/AD/wm-adsprop-notify-error">WM_ADSPROP_NOTIFY_ERROR</a>
---
UID: NF:strmif.IAMVfwCaptureDialogs.SendDriverMessage
title: IAMVfwCaptureDialogs::SendDriverMessage (strmif.h)
description: The SendDriverMessage method sends a driver-specific message. (IAMVfwCaptureDialogs.SendDriverMessage)
helpviewer_keywords: ["IAMVfwCaptureDialogs interface [DirectShow]","SendDriverMessage method","IAMVfwCaptureDialogs.SendDriverMessage","IAMVfwCaptureDialogs::SendDriverMessage","IAMVfwCaptureDialogsSendDriverMessage","SendDriverMessage","SendDriverMessage method [DirectShow]","SendDriverMessage method [DirectShow]","IAMVfwCaptureDialogs interface","dshow.iamvfwcapturedialogs_senddrivermessage","strmif/IAMVfwCaptureDialogs::SendDriverMessage"]
old-location: dshow\iamvfwcapturedialogs_senddrivermessage.htm
tech.root: dshow
ms.assetid: 0a8ba932-0f31-4768-b5e3-15ec8533a574
ms.date: 12/05/2018
ms.keywords: IAMVfwCaptureDialogs interface [DirectShow],SendDriverMessage method, IAMVfwCaptureDialogs.SendDriverMessage, IAMVfwCaptureDialogs::SendDriverMessage, IAMVfwCaptureDialogsSendDriverMessage, SendDriverMessage, SendDriverMessage method [DirectShow], SendDriverMessage method [DirectShow],IAMVfwCaptureDialogs interface, dshow.iamvfwcapturedialogs_senddrivermessage, strmif/IAMVfwCaptureDialogs::SendDriverMessage
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVfwCaptureDialogs::SendDriverMessage
 - strmif/IAMVfwCaptureDialogs::SendDriverMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCaptureDialogs.SendDriverMessage
---

# IAMVfwCaptureDialogs::SendDriverMessage


## -description

The <code>SendDriverMessage</code> method sends a driver-specific message.

## -parameters

### -param iDialog [in]

Handle of the driver dialog box. This is a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs">VfwCaptureDialogs</a> enumeration.

### -param uMsg [in]

Message to send to the driver.

### -param dw1 [in]

Message data.

### -param dw2 [in]

Message data.

## -returns

Return value varies depending on the implementation within each driver.

## -remarks

You should never need to use this method. This method can send any private message to the capture driver. Behavior might be undetermined in response to arbitrary messages; use this method at your own risk.

This method calls the Video for Windows <b>videoMessage</b> function to send the driver message.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcapturedialogs">IAMVfwCaptureDialogs Interface</a>

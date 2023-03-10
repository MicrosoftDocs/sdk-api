---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsNewClass0Message
title: IMbnSmsEvents::OnSmsNewClass0Message (mbnapi.h)
description: Notification method signaling the arrival of a new class 0/flash message.
helpviewer_keywords: ["IMbnSmsEvents interface [Microsoft Broadband Networks]","OnSmsNewClass0Message method","IMbnSmsEvents.OnSmsNewClass0Message","IMbnSmsEvents::OnSmsNewClass0Message","OnSmsNewClass0Message","OnSmsNewClass0Message method [Microsoft Broadband Networks]","OnSmsNewClass0Message method [Microsoft Broadband Networks]","IMbnSmsEvents interface","mbn.imbnsmsevents_onsmsnewclass0message","mbnapi/IMbnSmsEvents::OnSmsNewClass0Message"]
old-location: mbn\imbnsmsevents_onsmsnewclass0message.htm
tech.root: mbn
ms.assetid: e6d13393-557c-462c-a640-2228ab0c9c17
ms.date: 12/05/2018
ms.keywords: IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsNewClass0Message method, IMbnSmsEvents.OnSmsNewClass0Message, IMbnSmsEvents::OnSmsNewClass0Message, OnSmsNewClass0Message, OnSmsNewClass0Message method [Microsoft Broadband Networks], OnSmsNewClass0Message method [Microsoft Broadband Networks],IMbnSmsEvents interface, mbn.imbnsmsevents_onsmsnewclass0message, mbnapi/IMbnSmsEvents::OnSmsNewClass0Message
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnSmsEvents::OnSmsNewClass0Message
 - mbnapi/IMbnSmsEvents::OnSmsNewClass0Message
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsEvents.OnSmsNewClass0Message
---

# IMbnSmsEvents::OnSmsNewClass0Message


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method signaling the arrival of a new class 0/flash message.

## -parameters

### -param sms [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface representing the Mobile Broadband device that received the new message(s).

### -param smsFormat [in]

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_format">MBN_SMS_FORMAT</a> value that defines the format of the new SMS message.

### -param readMsgs [in]

An array of new messages.

## -returns

This method must return <b>S_OK</b>.

## -remarks

For GSM devices, the calling application should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on each element in <i>readMsgs</i> for an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgpdu">IMbnSmsReadMsgPdu</a> interface.

For CDMA devices, if <i>smsFormat</i> is <b>MBN_SMS_FORMAT_TEXT</b>, then the calling application should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for a <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgtextcdma">IMbnSmsReadMsgTextCdma</a> interface. If <i>smsFormat</i> is <b>MBN_SMS_FORMAT_PDU</b>, then the calling application should call <b>QueryInterface</b> for a <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgpdu">IMbnSmsReadMsgPdu</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>
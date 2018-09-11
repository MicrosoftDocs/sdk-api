---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsNewClass0Message
title: IMbnSmsEvents::OnSmsNewClass0Message
author: windows-sdk-content
description: Notification method signaling the arrival of a new class 0/flash message.
old-location: mbn\imbnsmsevents_onsmsnewclass0message.htm
tech.root: mbn
ms.assetid: e6d13393-557c-462c-a640-2228ab0c9c17
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsNewClass0Message method, IMbnSmsEvents.OnSmsNewClass0Message, IMbnSmsEvents::OnSmsNewClass0Message, OnSmsNewClass0Message, OnSmsNewClass0Message method [Microsoft Broadband Networks], OnSmsNewClass0Message method [Microsoft Broadband Networks],IMbnSmsEvents interface, mbn.imbnsmsevents_onsmsnewclass0message, mbnapi/IMbnSmsEvents::OnSmsNewClass0Message
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsEvents.OnSmsNewClass0Message
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnSmsEvents::OnSmsNewClass0Message


## -description


Notification method signaling the arrival of a new class 0/flash message.


## -parameters




### -param sms [in]

An <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface representing the Mobile Broadband device that received the new message(s).


### -param smsFormat [in]

An <a href="https://msdn.microsoft.com/ece079e2-43a2-4ca9-9aa7-1b9484f0176e">MBN_SMS_FORMAT</a> value that defines the format of the new SMS message.


### -param readMsgs [in]

An array of new messages.


## -returns



This method must return <b>S_OK</b>.




## -remarks



For GSM devices, the calling application should call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on each element in <i>readMsgs</i> for an <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface.

For CDMA devices, if <i>smsFormat</i> is <b>MBN_SMS_FORMAT_TEXT</b>, then the calling application should call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for a <a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a> interface. If <i>smsFormat</i> is <b>MBN_SMS_FORMAT_PDU</b>, then the calling application should call <b>QueryInterface</b> for a <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface. 




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 


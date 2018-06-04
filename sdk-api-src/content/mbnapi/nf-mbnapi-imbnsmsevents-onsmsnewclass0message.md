---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



For GSM devices, the calling application should call <a href="_com_IUnknown_QueryInterface">QueryInterface</a> on each element in <i>readMsgs</i> for an <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface.

For CDMA devices, if <i>smsFormat</i> is <b>MBN_SMS_FORMAT_TEXT</b>, then the calling application should call <a href="_com_IUnknown_QueryInterface">QueryInterface</a> for a <a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a> interface. If <i>smsFormat</i> is <b>MBN_SMS_FORMAT_PDU</b>, then the calling application should call <b>QueryInterface</b> for a <a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a> interface. 




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 


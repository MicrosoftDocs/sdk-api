---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsStatusChange
title: IMbnSmsEvents::OnSmsStatusChange method
author: windows-driver-content
description: Notification method indicating a change in the status of the message store.
old-location: mbn\imbnsmsevents_onsmsstatuschange.htm
old-project: mbn
ms.assetid: 8a3027e2-f8ee-476a-96e2-29ef4d87db38
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnSmsEvents, IMbnSmsEvents interface [Microsoft Broadband Networks], OnSmsStatusChange method, IMbnSmsEvents::OnSmsStatusChange, OnSmsStatusChange method [Microsoft Broadband Networks], OnSmsStatusChange method [Microsoft Broadband Networks], IMbnSmsEvents interface, OnSmsStatusChange,IMbnSmsEvents.OnSmsStatusChange, mbn.imbnsmsevents_onsmsstatuschange, mbnapi/IMbnSmsEvents::OnSmsStatusChange
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsEvents.OnSmsStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsEvents::OnSmsStatusChange method


## -description


Notification method indicating  a change in the status of the message store.


## -parameters




### -param sms [in]

An <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface representing the Mobile Broadband device for which the message store status has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use the <a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a> interface to get the new status information.  




## -see-also




<a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>
 

 


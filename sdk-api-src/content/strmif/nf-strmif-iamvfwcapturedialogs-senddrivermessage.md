---
UID: NF:strmif.IAMVfwCaptureDialogs.SendDriverMessage
title: IAMVfwCaptureDialogs::SendDriverMessage
author: windows-sdk-content
description: The SendDriverMessage method sends a driver-specific message.
old-location: dshow\iamvfwcapturedialogs_senddrivermessage.htm
old-project: DirectShow
ms.assetid: 0a8ba932-0f31-4768-b5e3-15ec8533a574
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IAMVfwCaptureDialogs interface [DirectShow],SendDriverMessage method, IAMVfwCaptureDialogs.SendDriverMessage, IAMVfwCaptureDialogs::SendDriverMessage, IAMVfwCaptureDialogsSendDriverMessage, SendDriverMessage, SendDriverMessage method [DirectShow], SendDriverMessage method [DirectShow],IAMVfwCaptureDialogs interface, dshow.iamvfwcapturedialogs_senddrivermessage, strmif/IAMVfwCaptureDialogs::SendDriverMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCaptureDialogs::SendDriverMessage


## -description



The <code>SendDriverMessage</code> method sends a driver-specific message.




## -parameters




### -param iDialog [in]

Handle of the driver dialog box. This is a member of the <a href="https://msdn.microsoft.com/0465d887-6452-4a67-9f52-a459620d12d2">VfwCaptureDialogs</a> enumeration.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5198c80c-28f3-4b5c-9b3b-aa502bf3a384">IAMVfwCaptureDialogs Interface</a>
 

 


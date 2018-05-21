---
UID: NF:strmif.IAMVfwCompressDialogs.SendDriverMessage
title: IAMVfwCompressDialogs::SendDriverMessage
author: windows-driver-content
description: The SendDriverMessage method sends a driver-specific message.
old-location: dshow\iamvfwcompressdialogs_senddrivermessage.htm
old-project: DirectShow
ms.assetid: b1558888-a8aa-416a-bb5b-a33a66dcb913
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMVfwCompressDialogs interface [DirectShow],SendDriverMessage method, IAMVfwCompressDialogs.SendDriverMessage, IAMVfwCompressDialogs::SendDriverMessage, IAMVfwCompressDialogsSendDriverMessage, SendDriverMessage, SendDriverMessage method [DirectShow], SendDriverMessage method [DirectShow],IAMVfwCompressDialogs interface, dshow.iamvfwcompressdialogs_senddrivermessage, strmif/IAMVfwCompressDialogs::SendDriverMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVfwCompressDialogs.SendDriverMessage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCompressDialogs::SendDriverMessage


## -description



The <code>SendDriverMessage</code> method sends a driver-specific message.




## -parameters




### -param uMsg [in]

Message to send to the driver.


### -param dw1 [in]

Message data.


### -param dw2 [in]

Message data.


## -returns



Return value varies depending on the implementation within each driver.




## -remarks



You should never need to use this method. This method can send any private message to the video compressor (codec). Behavior might be undetermined in response to arbitrary messages; use this method at your own risk.

This method calls the Video for Windows video compression manager (VCM) <a href="https://msdn.microsoft.com/0f9c37a9-4bf7-4c49-8a6a-81fbfa76d096">ICSendMessage</a> function to send the message.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5cc23d68-e0e6-401a-8d16-63c8c68af241">IAMVfwCompressDialogs Interface</a>
 

 


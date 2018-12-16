---
UID: NF:mfmediaengine.IMFMediaKeySessionNotify.KeyMessage
title: IMFMediaKeySessionNotify::KeyMessage
author: windows-sdk-content
description: Passes information to the application so it can initiate a key acquisition.
old-location: mf\imfmediakeysessionnotify_keymessage.htm
tech.root: medfound
ms.assetid: 50b0eb38-a212-4c89-80e8-83472b3d45ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaKeySessionNotify interface [Media Foundation],KeyMessage method, IMFMediaKeySessionNotify.KeyMessage, IMFMediaKeySessionNotify::KeyMessage, KeyMessage, KeyMessage method [Media Foundation], KeyMessage method [Media Foundation],IMFMediaKeySessionNotify interface, mf.imfmediakeysessionnotify_keymessage, mfmediaengine/IMFMediaKeySessionNotify::KeyMessage
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFMediaKeySessionNotify.KeyMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaKeySessionNotify::KeyMessage


## -description


Passes information to the application so it can initiate a key acquisition.


## -parameters




### -param destinationURL

The URL to send the message to.


### -param message

The message to send to the application.


### -param cb

The length in bytes of <i>message</i>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d28c16a8-4a74-40c3-be95-ff7e4b1cdc09">IMFMediaKeySessionNotify</a>
 

 


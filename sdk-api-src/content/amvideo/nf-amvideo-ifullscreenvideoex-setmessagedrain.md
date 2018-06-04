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

# IFullScreenVideoEx::SetMessageDrain


## -description



The <code>SetMessageDrain</code> method specifies a window to receive mouse and keyboard messages from the video window.




## -parameters




### -param hwnd [in]

Specifies a handle to the message-drain window.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is equivalent to the <a href="https://msdn.microsoft.com/aaf8624c-b3ea-4034-845a-6cd74c725c44">IVideoWindow::put_MessageDrain</a> method.

The Full Screen video renderer posts all mouse and keyboard messages to the window designated as a message drain. The exact list of messages that are posted is the same as the list given in <b>put_MessageDrain</b>.

Applications do not need to use this method. Instead, call the Filter Graph Manager's <b>put_MessageDrain</b> method before switching to full-screen mode. The Filter Graph Manager automatically sets the same message drain on the renderer that it selects for full-screen mode.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 


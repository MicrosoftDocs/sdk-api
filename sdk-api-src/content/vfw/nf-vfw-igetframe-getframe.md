---
UID: NF:vfw.IGetFrame.GetFrame
title: IGetFrame::GetFrame (vfw.h)
author: windows-sdk-content
description: The GetFrame method retrieves a decompressed copy of a frame from a stream. Called when an application uses the AVIStreamGetFrame function.
old-location: multimedia\igetframe_getframe.htm
tech.root: Multimedia
ms.assetid: e2b76aad-e2db-4e04-be54-b697830e8644
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFrame, GetFrame method [Windows Multimedia], GetFrame method [Windows Multimedia],IGetFrame interface, IGetFrame interface [Windows Multimedia],GetFrame method, IGetFrame.GetFrame, IGetFrame::GetFrame, _win32_IGetFrame_GetFrame, multimedia.igetframe_getframe, vfw/IGetFrame::GetFrame
ms.topic: method
f1_keywords: ["vfw/IGetFrame.GetFrame"]
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IGetFrame.GetFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetFrame::GetFrame


## -description



The <b>GetFrame</b> method retrieves a decompressed copy of a frame from a stream. Called when an application uses the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avistreamgetframe">AVIStreamGetFrame</a> function.




## -parameters




### -param lPos

Frame to copy and decompress.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the address of the decompressed frame data.




## -remarks



For handlers written in C++, <b>GetFrame</b> has the following syntax:


```cpp

LPVOID GetFrame(LONG lPos); 
 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
 

 


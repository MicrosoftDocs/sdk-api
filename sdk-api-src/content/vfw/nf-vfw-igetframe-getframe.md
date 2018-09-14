---
UID: NF:vfw.IGetFrame.GetFrame
title: IGetFrame::GetFrame
author: windows-sdk-content
description: The GetFrame method retrieves a decompressed copy of a frame from a stream. Called when an application uses the AVIStreamGetFrame function.
old-location: multimedia\igetframe_getframe.htm
tech.root: Multimedia
ms.assetid: e2b76aad-e2db-4e04-be54-b697830e8644
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetFrame, GetFrame method [Windows Multimedia], GetFrame method [Windows Multimedia],IGetFrame interface, IGetFrame interface [Windows Multimedia],GetFrame method, IGetFrame.GetFrame, IGetFrame::GetFrame, _win32_IGetFrame_GetFrame, multimedia.igetframe_getframe, vfw/IGetFrame::GetFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IGetFrame::GetFrame


## -description



The <b>GetFrame</b> method retrieves a decompressed copy of a frame from a stream. Called when an application uses the <a href="https://msdn.microsoft.com/9677efee-4c40-4acd-8911-eedcbee67d6b">AVIStreamGetFrame</a> function.




## -parameters




### -param lPos

Frame to copy and decompress.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the address of the decompressed frame data.




## -remarks



For handlers written in C++, <b>GetFrame</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LPVOID GetFrame(LONG lPos); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


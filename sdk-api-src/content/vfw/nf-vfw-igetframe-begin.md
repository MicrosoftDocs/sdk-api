---
UID: NF:vfw.IGetFrame.Begin
title: IGetFrame::Begin
author: windows-sdk-content
description: The Begin method prepares to extract and decompress copies of frames from a stream. Called when an application uses the AVIStreamGetFrameOpen function.
old-location: multimedia\igetframe_begin.htm
tech.root: Multimedia
ms.assetid: 2d2c1872-e0c3-4fea-bfb9-45b814973072
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Begin, Begin method [Windows Multimedia], Begin method [Windows Multimedia],IGetFrame interface, IGetFrame interface [Windows Multimedia],Begin method, IGetFrame.Begin, IGetFrame::Begin, _win32_IGetFrame_Begin, multimedia.igetframe_begin, vfw/IGetFrame::Begin
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
 - IGetFrame.Begin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetFrame::Begin


## -description



The <b>Begin</b> method prepares to extract and decompress copies of frames from a stream. Called when an application uses the <a href="https://msdn.microsoft.com/467560b2-f79f-49ab-b019-d6315f0c2030">AVIStreamGetFrameOpen</a> function.




## -parameters




### -param lStart

Starting frame for extracting and decompressing.


### -param lEnd

Ending frame for extracting and decompressing.


### -param lRate

Speed at which the file is read relative to its normal playback rate. Normal speed is 1000. Larger values indicate faster speeds; smaller values indicate slower speeds.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Begin</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Begin(LONG lStart, LONG lEnd, LONG lRate); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


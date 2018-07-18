---
UID: NF:vfw.IAVIStreaming.Begin
title: IAVIStreaming::Begin
author: windows-sdk-content
description: The Begin method prepares for the streaming operation. Called when an application uses the AVIStreamBeginStreaming function.
old-location: multimedia\iavistreaming_begin.htm
old-project: Multimedia
ms.assetid: 9bd76fc3-6c31-4e29-b482-82ee0a505656
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Begin, Begin method [Windows Multimedia], Begin method [Windows Multimedia],IAVIStreaming interface, IAVIStreaming interface [Windows Multimedia],Begin method, IAVIStreaming.Begin, IAVIStreaming::Begin, _win32_IAVIStreaming_Begin, multimedia.iavistreaming_begin, vfw/IAVIStreaming::Begin
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStreaming.Begin
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIStreaming::Begin


## -description



The <b>Begin</b> method prepares for the streaming operation. Called when an application uses the <a href="https://msdn.microsoft.com/79bf7c19-56b6-48fa-a673-32ce1bcdddad">AVIStreamBeginStreaming</a> function.




## -parameters




### -param lStart

Starting frame for streaming.


### -param lEnd

Ending frame for streaming.


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
 

 


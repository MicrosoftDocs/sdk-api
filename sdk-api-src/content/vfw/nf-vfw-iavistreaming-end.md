---
UID: NF:vfw.IAVIStreaming.End
title: IAVIStreaming::End
author: windows-driver-content
description: The End method ends the streaming operation. Called when an application uses the AVIStreamEndStreaming function.
old-location: multimedia\iavistreaming_end.htm
old-project: Multimedia
ms.assetid: 5db48b61-5926-41fb-9d0d-f39cba6deec9
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: End, End method [Windows Multimedia], End method [Windows Multimedia],IAVIStreaming interface, IAVIStreaming interface [Windows Multimedia],End method, IAVIStreaming.End, IAVIStreaming::End, _win32_IAVIStreaming_End, multimedia.iavistreaming_end, vfw/IAVIStreaming::End
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IAVIStreaming.End
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIStreaming::End


## -description



The <b>End</b> method ends the streaming operation. Called when an application uses the <a href="https://msdn.microsoft.com/8555bc24-c017-4d02-854b-e64cf9e8ae1b">AVIStreamEndStreaming</a> function.




## -parameters






#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>End</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT End(VOID); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


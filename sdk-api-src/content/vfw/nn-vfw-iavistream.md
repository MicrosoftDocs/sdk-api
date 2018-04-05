---
UID: NN:vfw.IAVIStream
title: IAVIStream
author: windows-driver-content
description: The IAVIStream interface supports creating and manipulating data streams within a file. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
The IAVIStream interface supports creating and manipulating data streams within a file. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavistream.htm
old-project: Multimedia
ms.assetid: 25f67f04-e005-48ee-89e7-a6ef89f6d6c6
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAVIStream, IAVIStream interface [Windows Multimedia], IAVIStream interface [Windows Multimedia], described, _win32_IAVIStream, multimedia.iavistream, vfw/IAVIStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IAVIStream
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# IAVIStream interface


## -description



The <b>IAVIStream</b> interface supports creating and manipulating data streams within a file. Uses <a href="https://msdn.microsoft.com/6db0af58-51ee-499a-81c4-4bce8aae0f06">IUnknown::QueryInterface</a>, <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a>, <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAVIStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/512ce9f8-f96c-4ef4-be1f-234165219ff7">Create</a>
</td>
<td align="left" width="63%">
Initializes a stream handler that is not associated with any file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0872023e-a760-4080-99da-df2941b84611">Delete</a>
</td>
<td align="left" width="63%">
Deletes data from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77927e6c-beee-4774-b727-5cd608cefb3d">FindSample</a>
</td>
<td align="left" width="63%">
Obtains the position in a stream of a key frame or a nonempty frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c58c4d68-4d27-4c3c-a1f6-bdafa3633dae">Info</a>
</td>
<td align="left" width="63%">
Fills and returns an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure with information about a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>
</td>
<td align="left" width="63%">
Reads data from a stream and copies it to an application-defined buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/688a19fb-5774-4e05-b0e8-4a98922def89">ReadData</a>
</td>
<td align="left" width="63%">
Reads data headers, format data, or nonaudio and nonvideo data. (Use the Read method to read audio and video data.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec684a91-9a16-4e9d-9d52-8b721df24889">ReadFormat</a>
</td>
<td align="left" width="63%">
Obtains format information from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8693ce01-1f73-4d1b-ba8a-12f6453def22">SetFormat</a>
</td>
<td align="left" width="63%">
Sets format information in a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>
</td>
<td align="left" width="63%">
Writes data to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6fb8e25-b6f9-4134-bb63-0a96fea88db8">WriteData</a>
</td>
<td align="left" width="63%">
Writes data headers, format data, or nonaudio and nonvideo data. (Use the <b>Write</b> method to write audio and video data.)

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


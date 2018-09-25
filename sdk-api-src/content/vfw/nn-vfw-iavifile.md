---
UID: NN:vfw.IAVIFile
title: IAVIFile
author: windows-sdk-content
description: The IAVIFile interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses IUnknown::QueryInterface, IUnknown::AddRef, and IUnknown::Release in addition to the following custom methods:\_
The IAVIFile interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses IUnknown::QueryInterface, IUnknown::AddRef, and IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavifile.htm
tech.root: Multimedia
ms.assetid: 401db941-cbf6-452b-84e2-605fafac8a6d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IAVIFile, IAVIFile interface [Windows Multimedia], IAVIFile interface [Windows Multimedia],described, _win32_IAVIFile, multimedia.iavifile, vfw/IAVIFile
ms.prod: windows
ms.technology: windows-sdk
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
 - IAVIFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIFile interface


## -description



The <b>IAVIFile</b> interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses <a href="https://msdn.microsoft.com/6db0af58-51ee-499a-81c4-4bce8aae0f06">IUnknown::QueryInterface</a>, <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a>, and <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIFile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAVIFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c922bb0-53ca-4285-861a-4701503b0445">CreateStream</a>
</td>
<td align="left" width="63%">
Creates a stream for writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43c4edbf-d736-4d85-9726-123f92145134">EndRecord</a>
</td>
<td align="left" width="63%">
Writes the "REC" chunk in a tightly interleaved AVI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66ab2d8f-39f5-4eec-a873-c6f554e3b8ff">GetStream</a>
</td>
<td align="left" width="63%">
Opens a stream by accessing it in a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cac01da4-b979-4386-8fc7-f47a7771e6f4">Info</a>
</td>
<td align="left" width="63%">
Fills and returns an <a href="https://msdn.microsoft.com/10d7decf-a133-4d55-93d5-867952307819">AVIFileInfo</a> structure with information about a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52071d08-1e95-4b4b-b85c-3fcca2c666aa">ReadData</a>
</td>
<td align="left" width="63%">
Reads file headers data, format data, or nonaudio and nonvideo data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b693a98-a91a-4fba-99da-e3bac71c1b22">WriteData</a>
</td>
<td align="left" width="63%">
Writes file headers data, format data, or nonaudio and nonvideo data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


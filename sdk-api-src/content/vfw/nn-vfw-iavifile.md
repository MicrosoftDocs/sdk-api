---
UID: NN:vfw.IAVIFile
title: IAVIFile (vfw.h)
author: windows-sdk-content
description: The IAVIFile interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses IUnknown::QueryInterface, IUnknown::AddRef, and IUnknown::Release in addition to the following custom methods:\_
The IAVIFile interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses IUnknown::QueryInterface, IUnknown::AddRef, and IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavifile.htm
tech.root: Multimedia
ms.assetid: 401db941-cbf6-452b-84e2-605fafac8a6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAVIFile, IAVIFile interface [Windows Multimedia], IAVIFile interface [Windows Multimedia],described, _win32_IAVIFile, multimedia.iavifile, vfw/IAVIFile
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
ms.custom: 19H1
---

# IAVIFile interface


## -description



The <b>IAVIFile</b> interface supports opening and manipulating files and file headers, and creating and obtaining stream interfaces. Uses <a href="https://docs.microsoft.com/previous-versions//dd757101(v=vs.85)">IUnknown::QueryInterface</a>, <a href="https://docs.microsoft.com/previous-versions//dd757100(v=vs.85)">IUnknown::AddRef</a>, and <a href="https://docs.microsoft.com/previous-versions//dd757102(v=vs.85)">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIFile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAVIFile</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-createstream">CreateStream</a>
</td>
<td align="left" width="63%">
Creates a stream for writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-endrecord">EndRecord</a>
</td>
<td align="left" width="63%">
Writes the "REC" chunk in a tightly interleaved AVI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Opens a stream by accessing it in a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-info">Info</a>
</td>
<td align="left" width="63%">
Fills and returns an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avifileinfo">AVIFileInfo</a> structure with information about a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-readdata">ReadData</a>
</td>
<td align="left" width="63%">
Reads file headers data, format data, or nonaudio and nonvideo data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavifile-writedata">WriteData</a>
</td>
<td align="left" width="63%">
Writes file headers data, format data, or nonaudio and nonvideo data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
 

 


---
UID: NN:mfreadwrite.IMFSinkWriterEx
title: IMFSinkWriterEx
author: windows-driver-content
description: Extends the IMFSinkWriter interface.
old-location: mf\imfsinkwriterex.htm
old-project: medfound
ms.assetid: 77E6CB22-E3B5-4D5E-8876-48582F75AA5C
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFSinkWriterEx, IMFSinkWriterEx interface [Media Foundation], IMFSinkWriterEx interface [Media Foundation], described, mf.imfsinkwriterex, mfreadwrite/IMFSinkWriterEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriterEx
product: Windows
targetos: Windows
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriterEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a> interface.

The <a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a> implements this interface in Windows 8. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the Sink Writer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterEx</b> interface inherits from <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>. <b>IMFSinkWriterEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72EEC01F-ED62-4DD7-A18C-766D01705CAE">GetTransformForStream</a>
</td>
<td align="left" width="63%">
Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 


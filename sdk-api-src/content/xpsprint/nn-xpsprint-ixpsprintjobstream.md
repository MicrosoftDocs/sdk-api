---
UID: NN:xpsprint.IXpsPrintJobStream
title: IXpsPrintJobStream
author: windows-sdk-content
description: A write-only stream interface into which an application writes print job data.
old-location: gdi\ixpsprintjobstream.htm
tech.root: printdocs
ms.assetid: a7855015-32db-48ff-8f8d-3d84d2843fde
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsPrintJobStream, IXpsPrintJobStream interface [Windows GDI], IXpsPrintJobStream interface [Windows GDI],described, gdi.ixpsprintjobstream, xpsprint/IXpsPrintJobStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.h
api_name:
 - IXpsPrintJobStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsPrintJobStream interface


## -description


<p class="CCE_Message">[IXpsPrintJobStream is not supported and may be altered or unavailable in the future. ]

A write-only stream interface into which an application writes print job data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsPrintJobStream</b> interface inherits from <a href="_stg_isequentialstream">ISequentialStream</a>. <b>IXpsPrintJobStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsPrintJobStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/259d0224-4e6e-43c8-905d-3529c781986a">Close</a>
</td>
<td align="left" width="63%">
Closes the stream and indicates that the entire document has been written.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/259d0224-4e6e-43c8-905d-3529c781986a">Close</a> method must be called before this interface is released.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">Documents</a>



<a href="_stg_isequentialstream">ISequentialStream</a>



<a href="https://msdn.microsoft.com/aa17e059-6208-4348-87f3-556a3818f2b9">IXpsPrintJob</a>



<a href="https://msdn.microsoft.com/d982ae2e-c68f-4197-b419-22a63e61db8a">StartXpsPrintJob</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


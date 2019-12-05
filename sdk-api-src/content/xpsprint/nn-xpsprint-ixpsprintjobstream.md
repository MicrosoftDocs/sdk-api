---
UID: NN:xpsprint.IXpsPrintJobStream
title: IXpsPrintJobStream (xpsprint.h)
description: A write-only stream interface into which an application writes print job data.
old-location: gdi\ixpsprintjobstream.htm
tech.root: printdocs
ms.assetid: a7855015-32db-48ff-8f8d-3d84d2843fde
ms.date: 12/05/2018
ms.keywords: IXpsPrintJobStream, IXpsPrintJobStream interface [Windows GDI], IXpsPrintJobStream interface [Windows GDI],described, gdi.ixpsprintjobstream, xpsprint/IXpsPrintJobStream
ms.topic: interface
f1_keywords:
- xpsprint/IXpsPrintJobStream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsPrintJobStream interface


## -description


<p class="CCE_Message">[IXpsPrintJobStream is not supported and may be altered or unavailable in the future. ]

A write-only stream interface into which an application writes print job data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsPrintJobStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>. <b>IXpsPrintJobStream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjobstream-close">Close</a>
</td>
<td align="left" width="63%">
Closes the stream and indicates that the entire document has been written.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjobstream-close">Close</a> method must be called before this interface is released.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob">StartXpsPrintJob</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


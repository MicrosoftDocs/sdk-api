---
UID: NN:xpsprint.IXpsPrintJob
title: IXpsPrintJob (xpsprint.h)

description: Provides access to a print job that is currently in progress.
old-location: gdi\ixpsprintjob.htm
tech.root: printdocs
ms.assetid: aa17e059-6208-4348-87f3-556a3818f2b9

ms.date: 12/05/2018
ms.keywords: IXpsPrintJob, IXpsPrintJob interface [Windows GDI], IXpsPrintJob interface [Windows GDI],described, gdi.ixpsprintjob, xpsprint/IXpsPrintJob
ms.topic: interface
f1_keywords: 
 - "xpsprint/IXpsPrintJob"
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
 - IXpsPrintJob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsPrintJob interface


## -description


<p class="CCE_Message">[IXpsPrintJob is not supported and may be altered or unavailable in the future. ]

Provides access to a print job that is currently in progress.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsPrintJob</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsPrintJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsPrintJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">GetJobStatus</a>
</td>
<td align="left" width="63%">
Gets the current status of the print job.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


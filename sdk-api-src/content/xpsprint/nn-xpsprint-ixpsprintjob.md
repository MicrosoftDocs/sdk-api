---
UID: NN:xpsprint.IXpsPrintJob
title: IXpsPrintJob
author: windows-driver-content
description: Provides access to a print job that is currently in progress.
old-location: gdi\ixpsprintjob.htm
old-project: printdocs
ms.assetid: aa17e059-6208-4348-87f3-556a3818f2b9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsPrintJob, IXpsPrintJob interface [Windows GDI], IXpsPrintJob interface [Windows GDI], described, gdi.ixpsprintjob, xpsprint/IXpsPrintJob
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_JOB_COMPLETION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	XpsPrint.h
api_name:
-	IXpsPrintJob
product: Windows
targetos: Windows
req.lib: XpsPrint.lib
req.dll: XpsPrint.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsPrintJob interface


## -description


<p class="CCE_Message">[IXpsPrintJob is not supported and may be altered or unavailable in the future. ]

Provides access to a print job that is currently in progress.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsPrintJob</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsPrintJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2a55aec-f8a5-40b4-8c26-1488df49eed0">GetJobStatus</a>
</td>
<td align="left" width="63%">
Gets the current status of the print job.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541159">Documents</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


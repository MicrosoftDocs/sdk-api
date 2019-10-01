---
UID: NN:imapi2.IDiscFormat2DataEventArgs
title: IDiscFormat2DataEventArgs (imapi2.h)
author: windows-sdk-content
description: Use this interface to retrieve information about the current write operation.
old-location: imapi\idiscformat2dataeventargs.htm
tech.root: imapi
ms.assetid: 6bf149d3-62ea-4ef5-8d45-44df9ad4982c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscFormat2DataEventArgs, IDiscFormat2DataEventArgs interface [IMAPI], IDiscFormat2DataEventArgs interface [IMAPI],described, imapi.idiscformat2dataeventargs, imapi2/IDiscFormat2DataEventArgs
ms.topic: interface
f1_keywords: 
 - "imapi2/IDiscFormat2DataEventArgs"
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2DataEventArgs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2DataEventArgs interface


## -description


Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2dataevents-update">DDiscFormat2DataEvents::Update</a> method that you implement.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2DataEventArgs</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>. <b>IDiscFormat2DataEventArgs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2DataEventArgs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2dataeventargs-get_currentaction">get_CurrentAction</a>
</td>
<td align="left" width="63%">
Retrieves the current write action being performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2dataeventargs-get_elapsedtime">get_ElapsedTime</a>
</td>
<td align="left" width="63%">
Retrieves the total elapsed time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2dataeventargs-get_remainingtime">get_RemainingTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated remaining time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2dataeventargs-get_totaltime">get_TotalTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated total time for write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
 

 


---
UID: NN:imapi2.IDiscFormat2TrackAtOnceEventArgs
title: IDiscFormat2TrackAtOnceEventArgs (imapi2.h)
description: Use this interface to retrieve information about the current write operation.
helpviewer_keywords: ["IDiscFormat2TrackAtOnceEventArgs","IDiscFormat2TrackAtOnceEventArgs interface [IMAPI]","IDiscFormat2TrackAtOnceEventArgs interface [IMAPI]","described","imapi.idiscformat2trackatonceeventargs","imapi2/IDiscFormat2TrackAtOnceEventArgs"]
old-location: imapi\idiscformat2trackatonceeventargs.htm
tech.root: imapi
ms.assetid: 4bbcc3e1-0c85-4ed8-bbf6-e172e5896ed9
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnceEventArgs, IDiscFormat2TrackAtOnceEventArgs interface [IMAPI], IDiscFormat2TrackAtOnceEventArgs interface [IMAPI],described, imapi.idiscformat2trackatonceeventargs, imapi2/IDiscFormat2TrackAtOnceEventArgs
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscFormat2TrackAtOnceEventArgs
 - imapi2/IDiscFormat2TrackAtOnceEventArgs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2TrackAtOnceEventArgs
---

# IDiscFormat2TrackAtOnceEventArgs interface


## -description

Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2trackatonceevents-update">DDiscFormat2TrackAtOnceEvents::Update</a> method that you implement.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2TrackAtOnceEventArgs</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>. <b>IDiscFormat2TrackAtOnceEventArgs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2TrackAtOnceEventArgs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonceeventargs-get_currentaction">get_CurrentAction</a>
</td>
<td align="left" width="63%">
Retrieves the current write action being performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonceeventargs-get_currenttracknumber">get_CurrentTrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the current track number being written to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonceeventargs-get_elapsedtime">get_ElapsedTime</a>
</td>
<td align="left" width="63%">
Retrieves the total elapsed time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonceeventargs-get_remainingtime">get_RemainingTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated remaining time of the write operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents">DDiscFormat2TrackAtOnceEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
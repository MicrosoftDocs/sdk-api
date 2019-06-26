---
UID: NN:imapi2.IDiscFormat2
title: IDiscFormat2 (imapi2.h)
author: windows-sdk-content
description: This is a base interface. Use the following interfaces which inherit this interface IDiscFormat2Data, IDiscFormat2Erase, IDiscFormat2TrackAtOnce, IDiscFormat2RawCD
old-location: imapi\idiscformat2.htm
tech.root: imapi
ms.assetid: c0bc2e8b-bd60-4c97-bd86-41963b20b1a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscFormat2, IDiscFormat2 interface [IMAPI], IDiscFormat2 interface [IMAPI],described, imapi.idiscformat2, imapi2/IDiscFormat2
ms.topic: interface
f1_keywords: 
 - "imapi2/IDiscFormat2"
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
 - IDiscFormat2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2 interface


## -description


This is a base interface. Use the following interfaces which inherit this interface:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDiscFormat2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank">get_MediaHeuristicallyBlank</a>
</td>
<td align="left" width="63%">
Attempts to determine if the media is blank using heuristics (mainly for DVD+RW and DVD-RAM media).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaphysicallyblank">get_MediaPhysicallyBlank</a>
</td>
<td align="left" width="63%">
Determines if the current media is reported as physically blank by the drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_supportedmediatypes">get_SupportedMediaTypes</a>
</td>
<td align="left" width="63%">
Retrieves the media types that the recorder supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-iscurrentmediasupported">IsCurrentMediaSupported</a>
</td>
<td align="left" width="63%">
Determines if the current media in a supported recorder supports the given format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-isrecordersupported">IsRecorderSupported</a>
</td>
<td align="left" width="63%">
Determines if the recorder supports the given format.

</td>
</tr>
</table> 


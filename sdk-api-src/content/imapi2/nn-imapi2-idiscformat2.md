---
UID: NN:imapi2.IDiscFormat2
title: IDiscFormat2 (imapi2.h)
author: windows-sdk-content
description: This is a base interface. Use the following interfaces which inherit this interface:\_

IDiscFormat2Data


IDiscFormat2Erase


IDiscFormat2TrackAtOnce


IDiscFormat2RawCD
old-location: imapi\idiscformat2.htm
tech.root: imapi
ms.assetid: c0bc2e8b-bd60-4c97-bd86-41963b20b1a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2, IDiscFormat2 interface [IMAPI], IDiscFormat2 interface [IMAPI],described, imapi.idiscformat2, imapi2/IDiscFormat2
ms.topic: interface
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
---

# IDiscFormat2 interface


## -description


This is a base interface. Use the following interfaces which inherit this interface:<ul>
<li>
<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>
</li>
<li>
<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IDiscFormat2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/28c410cc-5135-4443-8b86-e34676f14f51">get_MediaHeuristicallyBlank</a>
</td>
<td align="left" width="63%">
Attempts to determine if the media is blank using heuristics (mainly for DVD+RW and DVD-RAM media).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a797742-9142-415b-896b-09526894c2a6">get_MediaPhysicallyBlank</a>
</td>
<td align="left" width="63%">
Determines if the current media is reported as physically blank by the drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/281eacb5-f991-4d3f-95bb-6c2469d67a5c">get_SupportedMediaTypes</a>
</td>
<td align="left" width="63%">
Retrieves the media types that the recorder supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b4e8088-481e-4ff9-ba6d-aeca26287382">IsCurrentMediaSupported</a>
</td>
<td align="left" width="63%">
Determines if the current media in a supported recorder supports the given format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a96283a-a5a3-434a-834a-d539160cfc5c">IsRecorderSupported</a>
</td>
<td align="left" width="63%">
Determines if the recorder supports the given format.

</td>
</tr>
</table> 


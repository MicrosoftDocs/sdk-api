---
UID: NN:imapi2.IDiscFormat2TrackAtOnceEventArgs
title: IDiscFormat2TrackAtOnceEventArgs
author: windows-sdk-content
description: Use this interface to retrieve information about the current write operation.
old-location: imapi\idiscformat2trackatonceeventargs.htm
tech.root: imapi
ms.assetid: 4bbcc3e1-0c85-4ed8-bbf6-e172e5896ed9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDiscFormat2TrackAtOnceEventArgs, IDiscFormat2TrackAtOnceEventArgs interface [IMAPI], IDiscFormat2TrackAtOnceEventArgs interface [IMAPI],described, imapi.idiscformat2trackatonceeventargs, imapi2/IDiscFormat2TrackAtOnceEventArgs
ms.prod: windows
ms.technology: windows-sdk
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
 - IDiscFormat2TrackAtOnceEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2TrackAtOnceEventArgs interface


## -description


Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="https://msdn.microsoft.com/d63ff41d-993c-4f42-a4a3-f7c67f292a03">DDiscFormat2TrackAtOnceEvents::Update</a> method that you implement.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2TrackAtOnceEventArgs</b> interface inherits from <a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>. <b>IDiscFormat2TrackAtOnceEventArgs</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c4a0a07a-c80e-4dca-b3bb-8b2f26f969d8">get_CurrentAction</a>
</td>
<td align="left" width="63%">
Retrieves the current write action being performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e30afc06-b56b-49bc-8ad0-7446e16bdc95">get_CurrentTrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the current track number being written to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb7d2336-1ccd-4c0b-bd8b-5405a1de2c12">get_ElapsedTime</a>
</td>
<td align="left" width="63%">
Retrieves the total elapsed time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc427810-fcac-45a1-bd47-e392e1c0110e">get_RemainingTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated remaining time of the write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/15d88768-f6e9-4d0a-a132-08f89fb3c34f">DDiscFormat2TrackAtOnceEvents</a>



<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>
 

 


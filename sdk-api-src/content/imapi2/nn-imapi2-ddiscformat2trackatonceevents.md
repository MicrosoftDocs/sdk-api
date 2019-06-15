---
UID: NN:imapi2.DDiscFormat2TrackAtOnceEvents
title: DDiscFormat2TrackAtOnceEvents (imapi2.h)
author: windows-sdk-content
description: Implement this interface to receive notifications of the current track-writing operation.
old-location: imapi\ddiscformat2trackatonceevents.htm
tech.root: imapi
ms.assetid: 15d88768-f6e9-4d0a-a132-08f89fb3c34f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDiscFormat2TrackAtOnceEvents, DDiscFormat2TrackAtOnceEvents interface [IMAPI], DDiscFormat2TrackAtOnceEvents interface [IMAPI],described, imapi.ddiscformat2trackatonceevents, imapi2/DDiscFormat2TrackAtOnceEvents
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
 - DDiscFormat2TrackAtOnceEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DDiscFormat2TrackAtOnceEvents interface


## -description


Implement this interface to receive notifications of the current track-writing operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DDiscFormat2TrackAtOnceEvents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DDiscFormat2TrackAtOnceEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DDiscFormat2TrackAtOnceEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2trackatonceevents-update">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current track-writing operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>
 

 


---
UID: NN:tuner.IMPEG2Component
title: IMPEG2Component (tuner.h)
author: windows-sdk-content
description: The IMPEG2Component interface contains methods for getting and setting properties that describe an MPEG2 elementary stream.
old-location: mstv\impeg2component.htm
tech.root: mstv
ms.assetid: 63d1ae17-8e38-457e-98d7-e81e7576f1c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMPEG2Component, IMPEG2Component interface [Microsoft TV Technologies], IMPEG2Component interface [Microsoft TV Technologies],described, IMPEG2ComponentInterface, mstv.impeg2component, tuner/IMPEG2Component
ms.topic: interface
f1_keywords: ["tuner/IMPEG2Component"]
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IMPEG2Component
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2Component interface


## -description



The <b>IMPEG2Component</b> interface contains methods for getting and setting properties that describe an MPEG2 elementary stream. These properties are set by the TIF or Guide Store loader based on data in the transport stream tables. After the tune request is retrieved from the Guide Store and submitted either to the Video Control or directly to the Network Provider, these properties are used by the Network Provider and MPEG-2 Demultiplexer to acquire the specified substream and pass it to the downstream filters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2Component</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a>. <b>IMPEG2Component</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2Component</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-get_pcrpid">get_PCRPID</a>
</td>
<td align="left" width="63%">
Returns the MPEG2 Packet ID (PID) for this substream's time stamps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-get_pid">get_PID</a>
</td>
<td align="left" width="63%">
Get the packet identifier for this substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-get_programnumber">get_ProgramNumber</a>
</td>
<td align="left" width="63%">
Gets the program number, which provides a reverse lookup to PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-put_pcrpid">put_PCRPID</a>
</td>
<td align="left" width="63%">
Sets the MPEG2 Packet ID for this substream's time stamps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-put_pid">put_PID</a>
</td>
<td align="left" width="63%">
Set the packet identifier for this substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2component-put_programnumber">put_ProgramNumber</a>
</td>
<td align="left" width="63%">
Sets the program number, which provides a reverse lookup to PAT.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2Component)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 


---
UID: NN:sbe.IStreamBufferInitialize
title: IStreamBufferInitialize (sbe.h)
description: The IStreamBufferInitialize interface is used to configure the stream buffer filters. The Stream Buffer Source filter, Stream Buffer Sink filter, and StreamBufferConfig object all expose this interface.
old-location: mstv\istreambufferinitialize.htm
tech.root: mstv
ms.assetid: 357b2979-78de-4a99-bf52-4117af7dfaad
ms.date: 12/05/2018
ms.keywords: IStreamBufferInitialize, IStreamBufferInitialize interface [Microsoft TV Technologies], IStreamBufferInitialize interface [Microsoft TV Technologies],described, IStreamBufferInitializeInterface, mstv.istreambufferinitialize, sbe/IStreamBufferInitialize
f1_keywords:
- sbe/IStreamBufferInitialize
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
- Sbe.h
api_name:
- IStreamBufferInitialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferInitialize interface


## -description



The <b>IStreamBufferInitialize</b> interface is used to configure the stream buffer filters. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object all expose this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferInitialize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferInitialize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferInitialize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">SetHKEY</a>
</td>
<td align="left" width="63%">
Sets the registry key where the object stores configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-setsids">SetSIDs</a>
</td>
<td align="left" width="63%">
Sets the security identifiers (SIDs) that are used to protect access to the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferInitialize)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 


---
UID: NN:sbe.IStreamBufferConfigure3
title: IStreamBufferConfigure3 (sbe.h)
description: The IStreamBufferConfigure3 interface is exposed by the StreamBufferConfig object.
helpviewer_keywords: ["IStreamBufferConfigure3","IStreamBufferConfigure3 interface [Microsoft TV Technologies]","IStreamBufferConfigure3 interface [Microsoft TV Technologies]","described","IStreamBufferConfigure3Interface","mstv.istreambufferconfigure3","sbe/IStreamBufferConfigure3"]
old-location: mstv\istreambufferconfigure3.htm
tech.root: mstv
ms.assetid: 73f3cd43-11d1-4eff-861d-087bfda7d135
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure3, IStreamBufferConfigure3 interface [Microsoft TV Technologies], IStreamBufferConfigure3 interface [Microsoft TV Technologies],described, IStreamBufferConfigure3Interface, mstv.istreambufferconfigure3, sbe/IStreamBufferConfigure3
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferConfigure3
 - sbe/IStreamBufferConfigure3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure3
---

# IStreamBufferConfigure3 interface


## -description

The <b>IStreamBufferConfigure3</b> interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure3</b> interface inherits from <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure2">IStreamBufferConfigure2</a>. <b>IStreamBufferConfigure3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure3-getnamespace">GetNamespace</a>
</td>
<td align="left" width="63%">
Retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure3-getstartrecconfig">GetStartRecConfig</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">IStreamBufferRecordControl::Start</a> method automatically stops the current recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure3-setnamespace">SetNamespace</a>
</td>
<td align="left" width="63%">
Specifies a prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure3-setstartrecconfig">SetStartRecConfig</a>
</td>
<td align="left" width="63%">
Specifies whether the <b>IStreamBufferRecordControl::Start</b> method automatically stops the current recording.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure3)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure2">IStreamBufferConfigure2</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
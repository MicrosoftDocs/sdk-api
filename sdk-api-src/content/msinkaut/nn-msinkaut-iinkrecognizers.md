---
UID: NN:msinkaut.IInkRecognizers
title: IInkRecognizers (msinkaut.h)
author: windows-sdk-content
description: "."
old-location: tablet\iinkrecognizers.htm
tech.root: tablet
ms.assetid: 9BCCCFB1-567A-4CE7-9122-299A5AF52B08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkRecognizers, IInkRecognizers interface [Tablet PC], IInkRecognizers interface [Tablet PC],described, msinkaut/IInkRecognizers, tablet.iinkrecognizers
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkRecognizers"
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - msinkaut.h
api_name:
 - IInkRecognizers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizers interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizers</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognizers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRecognizers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer">GetDefaultRecognizer</a>
</td>
<td align="left" width="63%">
Retrieves the default recognizer for a known language, specified by a national language support (NLS) language code identifier (LCID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object at the specified index within the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)">InkRecognizers</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizers</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of objects or collections contained in a collection.

</td>
</tr>
</table> 


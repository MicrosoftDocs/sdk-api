---
UID: NN:msinkaut.IInkRecognizers
title: IInkRecognizers
author: windows-sdk-content
description: "."
old-location: tablet\iinkrecognizers.htm
tech.root: tablet
ms.assetid: 9BCCCFB1-567A-4CE7-9122-299A5AF52B08
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IInkRecognizers, IInkRecognizers interface [Tablet PC], IInkRecognizers interface [Tablet PC],described, msinkaut/IInkRecognizers, tablet.iinkrecognizers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizers interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizers</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognizers</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/499a257d-72de-4121-a98f-c827a3fef611">GetDefaultRecognizer</a>
</td>
<td align="left" width="63%">
Retrieves the default recognizer for a known language, specified by a national language support (NLS) language code identifier (LCID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65c169f0-fe61-4609-809c-52c53cfcba7f">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object at the specified index within the <a href="https://msdn.microsoft.com/b916e53f-9acd-40dc-961b-ebbecb15bd21">InkRecognizers</a> collection.

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

<a href="https://msdn.microsoft.com/4217f70e-9995-4a6d-ad13-21d3db2aca60">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of objects or collections contained in a collection.

</td>
</tr>
</table> 


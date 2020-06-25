---
UID: NN:micaut._IMathInputControlEvents
title: _IMathInputControlEvents (micaut.h)
description: Exposes the math input control event handlers.
helpviewer_keywords: ["_IMathInputControlEvents","_IMathInputControlEvents interface [Tablet PC]","_IMathInputControlEvents interface [Tablet PC]","described","micaut/_IMathInputControlEvents","tablet._imathinputcontrolevents"]
old-location: tablet\_imathinputcontrolevents.htm
tech.root: tablet
ms.assetid: e055ab45-53a8-4795-aff6-72987faad5ef
ms.date: 12/05/2018
ms.keywords: _IMathInputControlEvents, _IMathInputControlEvents interface [Tablet PC], _IMathInputControlEvents interface [Tablet PC],described, micaut/_IMathInputControlEvents, tablet._imathinputcontrolevents
f1_keywords:
- micaut/_IMathInputControlEvents
dev_langs:
- c++
req.header: micaut.h
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
- micaut.h
api_name:
- _IMathInputControlEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IMathInputControlEvents interface


## -description


The <b>_IMathInputControlEvents</b> interface exposes the math input control event handlers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">_IMathInputControlEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>_IMathInputControlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>_IMathInputControlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317350(v=vs.85)">Clear</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Clear</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)">Close</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Close</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)">Insert</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Insert</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317353(v=vs.85)">Paint</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the buttons and background of the control require painting.

</td>
</tr>
</table> 


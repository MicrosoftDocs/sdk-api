---
UID: NN:imapi2.DWriteEngine2Events
title: DWriteEngine2Events (imapi2.h)
description: Implement this interface to receive notifications of the current write operation.
helpviewer_keywords: ["DWriteEngine2Events","DWriteEngine2Events interface [IMAPI]","DWriteEngine2Events interface [IMAPI]","described","imapi.dwriteengine2events","imapi2/DWriteEngine2Events"]
old-location: imapi\dwriteengine2events.htm
tech.root: imapi
ms.assetid: 697f8247-6940-4b5e-8521-df89838837be
ms.date: 12/05/2018
ms.keywords: DWriteEngine2Events, DWriteEngine2Events interface [IMAPI], DWriteEngine2Events interface [IMAPI],described, imapi.dwriteengine2events, imapi2/DWriteEngine2Events
f1_keywords:
- imapi2/DWriteEngine2Events
dev_langs:
- c++
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
- DWriteEngine2Events
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWriteEngine2Events interface


## -description


Implement this interface to receive notifications of the current write operation.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DWriteEngine2Events</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>DWriteEngine2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DWriteEngine2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-dwriteengine2events-update">Update</a>
</td>
<td align="left" width="63%">
Implement this method to receive progress notification of the current write operation.

</td>
</tr>
</table> 


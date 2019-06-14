---
UID: NN:imepad.IImePad
title: IImePad (imepad.h)
author: windows-sdk-content
description: The IImePad interface inserts text into apps from IMEPadApplets that implement the IImePadApplet interface.
old-location: intl\iimepad.htm
tech.root: Intl
ms.assetid: 6604112A-5BD5-4B2C-AECC-D09180B04D7F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IImePad, IImePad interface [Internationalization for Windows Applications], IImePad interface [Internationalization for Windows Applications],described, imepad/IImePad, intl.iimepad
ms.topic: interface
req.header: imepad.h
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
 - Imepad.h
api_name:
 - IImePad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IImePad interface


## -description


The <b>IImePad</b> interface inserts text into apps from IMEPadApplets that implement the  <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> interface.

IMEPadApplets can insert their own strings into the current active app by calling <b>IImePad</b> and the  Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePad</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImePad</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImePad</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imepad/nf-imepad-iimepad-request">Request</a>
</td>
<td align="left" width="63%">
Called by an  <a href="https://docs.microsoft.com/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a> to insert text into an app.

</td>
</tr>
</table> 


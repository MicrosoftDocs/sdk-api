---
UID: NN:imepad.IImePad
title: IImePad
author: windows-driver-content
description: The IImePad interface inserts text into apps from IMEPadApplets that implement the IImePadApplet interface.
old-location: intl\iimepad.htm
old-project: Intl
ms.assetid: 6604112A-5BD5-4B2C-AECC-D09180B04D7F
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IImePad, IImePad interface [Internationalization for Windows Applications], IImePad interface [Internationalization for Windows Applications], described, imepad/IImePad, intl.iimepad
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Imepad.h
api_name:
-	IImePad
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IImePad interface


## -description


The <b>IImePad</b> interface inserts text into apps from IMEPadApplets that implement the  <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> interface.

IMEPadApplets can insert their own strings into the current active app by calling <b>IImePad</b> and the  Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePad</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IImePad</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554564">Request</a>
</td>
<td align="left" width="63%">
Called by an  <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> to insert text into an app.

</td>
</tr>
</table> 


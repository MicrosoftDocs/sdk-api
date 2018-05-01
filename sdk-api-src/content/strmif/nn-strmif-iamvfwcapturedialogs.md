---
UID: NN:strmif.IAMVfwCaptureDialogs
title: IAMVfwCaptureDialogs
author: windows-driver-content
description: The IAMVfwCaptureDialogs interface displays a dialog box provided by a Video for Windows (VFW) capture driver.The VFW Capture filter implements this interface.
old-location: dshow\iamvfwcapturedialogs.htm
old-project: DirectShow
ms.assetid: 5198c80c-28f3-4b5c-9b3b-aa502bf3a384
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMVfwCaptureDialogs, IAMVfwCaptureDialogs interface [DirectShow], IAMVfwCaptureDialogs interface [DirectShow], described, IAMVfwCaptureDialogsInterface, dshow.iamvfwcapturedialogs, strmif/IAMVfwCaptureDialogs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVfwCaptureDialogs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCaptureDialogs interface


## -description



The <code>IAMVfwCaptureDialogs</code> interface displays a dialog box provided by a Video for Windows (VFW) capture driver.

The <a href="https://msdn.microsoft.com/663b6b3b-2a50-4586-9506-600a59869abe">VFW Capture</a> filter implements this interface. Applications can use it to display one of the three dialog boxes (Source, Format, or Display) provided by VFW capture drivers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVfwCaptureDialogs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVfwCaptureDialogs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVfwCaptureDialogs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be2d9b1f-c53f-4a75-89ab-ec07c655cbea">HasDialog</a>
</td>
<td align="left" width="63%">
Determines if the specified dialog box exists in the driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a8ba932-0f31-4768-b5e3-15ec8533a574">SendDriverMessage</a>
</td>
<td align="left" width="63%">
Sends a driver-specific message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/988b68e5-12fb-47c5-8a49-81ba262da739">ShowDialog</a>
</td>
<td align="left" width="63%">
Displays the specified dialog box.

</td>
</tr>
</table> 


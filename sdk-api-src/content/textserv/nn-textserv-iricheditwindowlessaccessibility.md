---
UID: NN:textserv.IRicheditWindowlessAccessibility
title: IRicheditWindowlessAccessibility
author: windows-sdk-content
description: Enables the host container of a windowless rich edit control to obtain the Microsoft UI Automation provider for the parent of the control.
old-location: controls\iricheditwindowlessaccessibility.htm
tech.root: controls
ms.assetid: E58E9577-4004-4627-A0D6-CF8166C0C43F
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IRicheditWindowlessAccessibility, IRicheditWindowlessAccessibility interface [Windows Controls], IRicheditWindowlessAccessibility interface [Windows Controls],described, controls.iricheditwindowlessaccessibility, textserv/IRicheditWindowlessAccessibility
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRicheditWindowlessAccessibility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRicheditWindowlessAccessibility interface


## -description


Enables the host container of a windowless rich edit control to obtain the Microsoft UI Automation provider for the parent of the control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRicheditWindowlessAccessibility</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRicheditWindowlessAccessibility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRicheditWindowlessAccessibility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09245E4F-0D38-4C9F-8DD8-D6A2851AD256">CreateProvider</a>
</td>
<td align="left" width="63%">
Obtains a UI Automation provider object for the parent of a windowless rich edit control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/89C4DF55-F889-4ED6-8812-E2244A9F7BB8">IRichEditUiaInformation</a>



<a href="https://msdn.microsoft.com/2590002F-A6B0-4AA7-A54C-A5AB5304D9FA">IRichEditUiaOverrides</a>
 

 


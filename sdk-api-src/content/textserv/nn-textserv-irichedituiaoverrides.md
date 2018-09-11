---
UID: NN:textserv.IRicheditUiaOverrides
title: IRicheditUiaOverrides
author: windows-sdk-content
description: Enables the host container of a windowless rich edit control to override the control's Microsoft UI Automation accessibility properties.
old-location: controls\irichedituiaoverrides.htm
tech.root: controls
ms.assetid: 2590002F-A6B0-4AA7-A54C-A5AB5304D9FA
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRicheditUiaOverrides, IRicheditUiaOverrides interface [Windows Controls], IRicheditUiaOverrides interface [Windows Controls],described, controls.irichedituiaoverrides, textserv/IRicheditUiaOverrides
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
 - IRicheditUiaOverrides
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRicheditUiaOverrides interface


## -description


Enables the host  container of a windowless rich edit control to override the control's Microsoft UI Automation accessibility properties.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRicheditUiaOverrides</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRicheditUiaOverrides</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRicheditUiaOverrides</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C949A3DA-F98E-4035-8986-A76EB8F54558">GetPropertyOverrideValue</a>
</td>
<td align="left" width="63%">
Retrieves the host container's override value for the specified UI Automation accessibility property of a windowless rich edit control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh768428(v=VS.85).aspx">IRichEditUiaInformation</a>



<a href="https://msdn.microsoft.com/E58E9577-4004-4627-A0D6-CF8166C0C43F">IRicheditWindowlessAccessibility</a>
 

 


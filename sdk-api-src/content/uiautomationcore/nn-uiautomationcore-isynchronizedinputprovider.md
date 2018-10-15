---
UID: NN:uiautomationcore.ISynchronizedInputProvider
title: ISynchronizedInputProvider
author: windows-sdk-content
description: Enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.
old-location: winauto\uiauto_ISynchronizedInputProvider.htm
tech.root: WinAuto
ms.assetid: 70495eba-172a-432e-951d-1092fd676d5e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ISynchronizedInputProvider, ISynchronizedInputProvider interface [Windows Accessibility], ISynchronizedInputProvider interface [Windows Accessibility],described, uiauto.uiauto_ISynchronizedInputProvider, uiauto_ISynchronizedInputProvider, uiautomationcore/ISynchronizedInputProvider, winauto.uiauto_ISynchronizedInputProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ISynchronizedInputProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronizedInputProvider interface


## -description


Enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronizedInputProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISynchronizedInputProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronizedInputProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/388fd113-ec66-4152-a42a-a485edcb9b80">Cancel</a>
</td>
<td align="left" width="63%">
Cancels listening for input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad9e6ca3-b38c-41f8-9c61-ce51786672eb">StartListening</a>
</td>
<td align="left" width="63%">
Starts listening for input of the specified type. 

</td>
</tr>
</table> 


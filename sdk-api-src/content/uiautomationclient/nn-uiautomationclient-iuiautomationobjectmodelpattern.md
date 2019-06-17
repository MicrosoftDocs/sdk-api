---
UID: NN:uiautomationclient.IUIAutomationObjectModelPattern
title: IUIAutomationObjectModelPattern (uiautomationclient.h)
author: windows-sdk-content
description: Provides access to the underlying object model implemented by a control or application.
old-location: winauto\uiauto_IUIAutomationObjectModelPattern.htm
tech.root: WinAuto
ms.assetid: 044A1EE7-4CBD-45E3-A1A8-CA00DC03E136
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationObjectModelPattern, IUIAutomationObjectModelPattern interface [Windows Accessibility], IUIAutomationObjectModelPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationObjectModelPattern, winauto.uiauto_IUIAutomationObjectModelPattern
ms.topic: interface
f1_keywords: ["uiautomationclient/IUIAutomationObjectModelPattern"]
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationObjectModelPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationObjectModelPattern interface


## -description


Provides access to the underlying object model implemented by a control or application. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationObjectModelPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationObjectModelPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationObjectModelPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel">GetUnderlyingObjectModel</a>
</td>
<td align="left" width="63%">
Retrieves an interface used to access the underlying object model of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 


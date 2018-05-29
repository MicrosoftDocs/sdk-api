---
UID: NN:uiribbon.IUICommandHandler
title: IUICommandHandler
author: windows-sdk-content
description: The IUICommandHandler interface is implemented by the application and defines the methods for gathering Command information and handling Command events from the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuicommandhandler.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicommandhandler\iuicommandhandler.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IUICommandHandler, IUICommandHandler interface [Windows Ribbon], IUICommandHandler interface [Windows Ribbon],described, scenicintent_IUICommandHandler, uiribbon/IUICommandHandler, windowsribbon.windowsribbon_iuicommandhandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uiribbon.dll
api_name:
-	IUICommandHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
req.product: Windows UI
---

# IUICommandHandler interface


## -description



				The <b>IUICommandHandler</b> interface is implemented by the application and defines the methods for gathering Command information and handling Command events from the Windows Ribbon framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUICommandHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUICommandHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUICommandHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543208">Execute</a>
</td>
<td align="left" width="63%">
Responds to execute events on Commands bound to the Command handler.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47acd4d3-6841-4a19-99ff-d36fe78c2e93">UpdateProperty</a>
</td>
<td align="left" width="63%">

			Responds to property update requests from the Ribbon framework.
		

</td>
</tr>
</table> 


## -remarks




				For each Command in a View, the Ribbon framework requires a corresponding Command handler in 
				the host application. A new handler or an existing handler must be bound to the Command through 
				the <a href="https://msdn.microsoft.com/13e03acd-1a1e-48f9-b413-5a24d8b784d0">IUIApplication::OnCreateUICommand</a> notification method.
			


				Any number of Commands can be bound to a Command handler.
			


				The Command handler serves two purposes: respond to property update requests and respond to execute events on any Command to which it is bound.
			




## -see-also




<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 


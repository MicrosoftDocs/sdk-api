---
UID: NN:uiautomationclient.IUIAutomationEventHandlerGroup
title: IUIAutomationEventHandlerGroup (uiautomationclient.h)
description: Exposes methods for adding one or more events to a collection for bulk registration through the CreateEventHandlerGroup and AddEventHandlerGroup methods defined in IUIAutomation6.
helpviewer_keywords: ["IUIAutomationEventHandlerGroup","IUIAutomationEventHandlerGroup interface [Windows Accessibility]","IUIAutomationEventHandlerGroup interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationEventHandlerGroup","winauto.uiauto_IUIAutomationEventHandlerGroup"]
old-location: winauto\uiauto_IUIAutomationEventHandlerGroup.htm
tech.root: WinAuto
ms.assetid: 4D92FFD9-1E83-4DE3-B20C-5203E4D7E3A2
ms.date: 12/05/2018
ms.keywords: IUIAutomationEventHandlerGroup, IUIAutomationEventHandlerGroup interface [Windows Accessibility], IUIAutomationEventHandlerGroup interface [Windows Accessibility],described, uiautomationclient/IUIAutomationEventHandlerGroup, winauto.uiauto_IUIAutomationEventHandlerGroup
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - IUIAutomationEventHandlerGroup
 - uiautomationclient/IUIAutomationEventHandlerGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationEventHandlerGroup
---

# IUIAutomationEventHandlerGroup interface


## -description

Exposes methods for adding one or more events to a  collection for bulk registration through the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-createeventhandlergroup">CreateEventHandlerGroup</a> and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-addeventhandlergroup">AddEventHandlerGroup</a> methods defined in <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6">IUIAutomation6</a>. <div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> namespaces.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
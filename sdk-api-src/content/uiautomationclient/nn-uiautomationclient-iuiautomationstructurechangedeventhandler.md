---
UID: NN:uiautomationclient.IUIAutomationStructureChangedEventHandler
title: IUIAutomationStructureChangedEventHandler (uiautomationclient.h)
description: Exposes a method to handle events that occur when the Microsoft UI Automation tree structure is changed.
helpviewer_keywords: ["IUIAutomationStructureChangedEventHandler","IUIAutomationStructureChangedEventHandler interface [Windows Accessibility]","IUIAutomationStructureChangedEventHandler interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationStructureChangedEventHandler","uiauto_IUIAutomationStructureChangedEventHandler","uiautomationclient/IUIAutomationStructureChangedEventHandler","winauto.uiauto_IUIAutomationStructureChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationStructureChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: a28ad163-d931-432a-a786-646a10baaf86
ms.date: 12/05/2018
ms.keywords: IUIAutomationStructureChangedEventHandler, IUIAutomationStructureChangedEventHandler interface [Windows Accessibility], IUIAutomationStructureChangedEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationStructureChangedEventHandler, uiauto_IUIAutomationStructureChangedEventHandler, uiautomationclient/IUIAutomationStructureChangedEventHandler, winauto.uiauto_IUIAutomationStructureChangedEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - IUIAutomationStructureChangedEventHandler
 - uiautomationclient/IUIAutomationStructureChangedEventHandler
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
 - IUIAutomationStructureChangedEventHandler
---

# IUIAutomationStructureChangedEventHandler interface


## -description

Exposes a method to handle events that occur when the Microsoft UI Automation tree structure is changed.

## -inheritance

The <b>IUIAutomationStructureChangedEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationStructureChangedEventHandler</b> also has these types of members:

## -remarks

This interface is implemented by the application to handle events that it has subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler">AddStructureChangedEventHandler</a>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>

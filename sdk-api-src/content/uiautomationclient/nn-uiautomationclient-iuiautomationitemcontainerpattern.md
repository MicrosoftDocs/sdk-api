---
UID: NN:uiautomationclient.IUIAutomationItemContainerPattern
title: IUIAutomationItemContainerPattern (uiautomationclient.h)
description: Exposes a method that retrieves an item from a container, such as a virtual list.
helpviewer_keywords: ["IUIAutomationItemContainerPattern","IUIAutomationItemContainerPattern interface [Windows Accessibility]","IUIAutomationItemContainerPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationItemContainerPattern","uiauto_IUIAutomationItemContainerPattern","uiautomationclient/IUIAutomationItemContainerPattern","winauto.uiauto_IUIAutomationItemContainerPattern"]
old-location: winauto\uiauto_IUIAutomationItemContainerPattern.htm
tech.root: WinAuto
ms.assetid: 87655c25-d666-4349-9750-566b60b37c56
ms.date: 12/05/2018
ms.keywords: IUIAutomationItemContainerPattern, IUIAutomationItemContainerPattern interface [Windows Accessibility], IUIAutomationItemContainerPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationItemContainerPattern, uiauto_IUIAutomationItemContainerPattern, uiautomationclient/IUIAutomationItemContainerPattern, winauto.uiauto_IUIAutomationItemContainerPattern
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
 - IUIAutomationItemContainerPattern
 - uiautomationclient/IUIAutomationItemContainerPattern
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
 - IUIAutomationItemContainerPattern
---

# IUIAutomationItemContainerPattern interface


## -description

Exposes a method that retrieves an item from a container, such as a virtual list.

## -inheritance

The <b>IUIAutomationItemContainerPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationItemContainerPattern</b> also has these types of members:

## -remarks

This interface is not limited to use by virtualized containers. Any container that can implement efficient name lookup can support this <i>control pattern</i>, enabling clients to look up names more quickly than by using methods such as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>, which must traverse the Microsoft UI Automation tree.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

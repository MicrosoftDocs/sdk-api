---
UID: NN:uiautomationclient.IUIAutomationLegacyIAccessiblePattern
title: IUIAutomationLegacyIAccessiblePattern (uiautomationclient.h)
description: Exposes methods and properties that enable Microsoft UI Automation clients to retrieve UI information from Microsoft Active Accessibility (MSAA) servers.
helpviewer_keywords: ["IUIAutomationLegacyIAccessiblePattern","IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern","uiauto_IUIAutomationLegacyIAccessiblePattern","uiautomationclient/IUIAutomationLegacyIAccessiblePattern","winauto.uiauto_IUIAutomationLegacyIAccessiblePattern"]
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern.htm
tech.root: WinAuto
ms.assetid: d6564d14-a739-47bf-9202-0757ac3ba7f8
ms.date: 12/05/2018
ms.keywords: IUIAutomationLegacyIAccessiblePattern, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility], IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern, uiauto_IUIAutomationLegacyIAccessiblePattern, uiautomationclient/IUIAutomationLegacyIAccessiblePattern, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern
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
 - IUIAutomationLegacyIAccessiblePattern
 - uiautomationclient/IUIAutomationLegacyIAccessiblePattern
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
 - IUIAutomationLegacyIAccessiblePattern
---

# IUIAutomationLegacyIAccessiblePattern interface


## -description

Exposes methods and properties that enable Microsoft UI Automation clients to retrieve UI information from Microsoft Active Accessibility (MSAA) servers.

## -inheritance

The <b>IUIAutomationLegacyIAccessiblePattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationLegacyIAccessiblePattern</b> also has these types of members:

## -remarks

This interface is obtained just like any other control pattern. It enables UI Automation clients to gather MSAA properties more efficiently, taking advantage of the caching system, and also enables UI Automation clients to interact with native Microsoft Active Accessibility servers that support the <b>IAccessible</b> interface.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

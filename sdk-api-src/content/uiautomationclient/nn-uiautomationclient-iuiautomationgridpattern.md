---
UID: NN:uiautomationclient.IUIAutomationGridPattern
title: IUIAutomationGridPattern (uiautomationclient.h)
description: Provides access to a control that acts as a container for a collection of child controls that are organized in a two-dimensional logical coordinate system that can be traversed by row and column.
helpviewer_keywords: ["IUIAutomationGridPattern","IUIAutomationGridPattern interface [Windows Accessibility]","IUIAutomationGridPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationGridPattern","uiauto_IUIAutomationGridPattern","uiautomationclient/IUIAutomationGridPattern","winauto.uiauto_IUIAutomationGridPattern"]
old-location: winauto\uiauto_IUIAutomationGridPattern.htm
tech.root: WinAuto
ms.assetid: 36a4893e-5f49-413c-a29a-e58291c7d057
ms.date: 12/05/2018
ms.keywords: IUIAutomationGridPattern, IUIAutomationGridPattern interface [Windows Accessibility], IUIAutomationGridPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationGridPattern, uiauto_IUIAutomationGridPattern, uiautomationclient/IUIAutomationGridPattern, winauto.uiauto_IUIAutomationGridPattern
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
 - IUIAutomationGridPattern
 - uiautomationclient/IUIAutomationGridPattern
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
 - IUIAutomationGridPattern
---

# IUIAutomationGridPattern interface


## -description

Provides access to  a control that acts as a container for a collection of child controls that  are organized in a two-dimensional logical coordinate system that can be traversed by row and column. The children of this element support the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgriditempattern">IUIAutomationGridItemPattern</a> interface.

## -inheritance

The <b>IUIAutomationGridPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationGridPattern</b> also has these types of members:

## -remarks

This interface does not support active manipulation of a grid; the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a> interface is required for this functionality.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

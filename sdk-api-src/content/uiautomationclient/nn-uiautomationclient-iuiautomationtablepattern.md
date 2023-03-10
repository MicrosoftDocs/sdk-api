---
UID: NN:uiautomationclient.IUIAutomationTablePattern
title: IUIAutomationTablePattern (uiautomationclient.h)
description: Provides access to a control that acts as a container for a collection of child elements.
helpviewer_keywords: ["IUIAutomationTablePattern","IUIAutomationTablePattern interface [Windows Accessibility]","IUIAutomationTablePattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTablePattern","uiauto_IUIAutomationTablePattern","uiautomationclient/IUIAutomationTablePattern","winauto.uiauto_IUIAutomationTablePattern"]
old-location: winauto\uiauto_IUIAutomationTablePattern.htm
tech.root: WinAuto
ms.assetid: a393b323-31f9-4f31-abdb-7a0fb7c8ab96
ms.date: 12/05/2018
ms.keywords: IUIAutomationTablePattern, IUIAutomationTablePattern interface [Windows Accessibility], IUIAutomationTablePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTablePattern, uiauto_IUIAutomationTablePattern, uiautomationclient/IUIAutomationTablePattern, winauto.uiauto_IUIAutomationTablePattern
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
 - IUIAutomationTablePattern
 - uiautomationclient/IUIAutomationTablePattern
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
 - IUIAutomationTablePattern
---

# IUIAutomationTablePattern interface


## -description

Provides access to a control that acts as a container for a collection of child elements. The children of this element support <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtableitempattern">IUIAutomationTableItemPattern</a> and are organized in a two-dimensional logical coordinate system that can be traversed by row and column.

## -inheritance

The <b>IUIAutomationTablePattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTablePattern</b> also has these types of members:

## -remarks

This control pattern is analogous to <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a> with the distinction that any control that supports <b>IUIAutomationTablePattern</b> also exposes a column or row header relationship, or both, for each child element. Controls that support the <a href="/windows/desktop/WinAuto/uiauto-implementingtableitem">Table</a> control pattern also support the <a href="/windows/desktop/WinAuto/uiauto-implementinggrid">Grid</a> control pattern in order to provide access to the inherent grid functionality of a table.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

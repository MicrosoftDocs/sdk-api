---
UID: NN:uiautomationclient.IUIAutomationCondition
title: IUIAutomationCondition (uiautomationclient.h)
description: This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.
helpviewer_keywords: ["IUIAutomationCondition","IUIAutomationCondition interface [Windows Accessibility]","IUIAutomationCondition interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationCondition","uiauto_IUIAutomationCondition","uiautomationclient/IUIAutomationCondition","winauto.uiauto_IUIAutomationCondition"]
old-location: winauto\uiauto_IUIAutomationCondition.htm
tech.root: WinAuto
ms.assetid: 66515d42-2b98-4923-b326-9fec557345b7
ms.date: 12/05/2018
ms.keywords: IUIAutomationCondition, IUIAutomationCondition interface [Windows Accessibility], IUIAutomationCondition interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationCondition, uiauto_IUIAutomationCondition, uiautomationclient/IUIAutomationCondition, winauto.uiauto_IUIAutomationCondition
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
 - IUIAutomationCondition
 - uiautomationclient/IUIAutomationCondition
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
 - IUIAutomationCondition
---

# IUIAutomationCondition interface


## -description

This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree. This interface has no members. 
        

The following interfaces inherit from <b>IUIAutomationCondition</b>:
        <ul>
<li>
<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationandcondition">IUIAutomationAndCondition</a>
</li>
<li>
<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationboolcondition">IUIAutomationBoolCondition</a>
</li>
<li>
<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationnotcondition">IUIAutomationNotCondition</a>
</li>
<li>
<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationpropertycondition">IUIAutomationPropertyCondition</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<a href="/windows/desktop/WinAuto/uiauto-client-propconditioninterfaces">Property Condition Interfaces for Clients</a>
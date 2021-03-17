---
UID: NF:uiautomationclient.IUIAutomation.get_RawViewCondition
title: IUIAutomation::get_RawViewCondition (uiautomationclient.h)
description: Retrieves a predefined IUIAutomationCondition interface that selects all UI elements in an unfiltered view.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","RawViewCondition property","IUIAutomation.RawViewCondition","IUIAutomation.get_RawViewCondition","IUIAutomation::RawViewCondition","IUIAutomation::get_RawViewCondition","RawViewCondition property [Windows Accessibility]","RawViewCondition property [Windows Accessibility]","IUIAutomation interface","get_RawViewCondition","uiauto.uiauto_IUIAutomation_RawViewCondition","uiauto_IUIAutomation_RawViewCondition","uiautomationclient/IUIAutomation::RawViewCondition","uiautomationclient/IUIAutomation::get_RawViewCondition","winauto.uiauto_IUIAutomation_RawViewCondition"]
old-location: winauto\uiauto_IUIAutomation_RawViewCondition.htm
tech.root: WinAuto
ms.assetid: 2ed9867c-2bcb-464e-a5a6-15e9f4dcd276
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RawViewCondition property, IUIAutomation.RawViewCondition, IUIAutomation.get_RawViewCondition, IUIAutomation::RawViewCondition, IUIAutomation::get_RawViewCondition, RawViewCondition property [Windows Accessibility], RawViewCondition property [Windows Accessibility],IUIAutomation interface, get_RawViewCondition, uiauto.uiauto_IUIAutomation_RawViewCondition, uiauto_IUIAutomation_RawViewCondition, uiautomationclient/IUIAutomation::RawViewCondition, uiautomationclient/IUIAutomation::get_RawViewCondition, winauto.uiauto_IUIAutomation_RawViewCondition
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation::get_RawViewCondition
 - uiautomationclient/IUIAutomation::get_RawViewCondition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.RawViewCondition
 - IUIAutomation.get_RawViewCondition
---

# IUIAutomation::get_RawViewCondition


## -description

Retrieves a predefined <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a> interface that selects all UI elements in an unfiltered view.

This property is read-only.

## -parameters

## -remarks

Used by itself, the condition is functionally identical to the one retrieved by <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtruecondition">IUIAutomation::CreateTrueCondition</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_contentviewcondition">ContentViewCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_controlviewcondition">ControlViewCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<b>Reference</b>
---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.Select
title: IUIAutomationLegacyIAccessiblePattern::Select (uiautomationclient.h)
description: Performs a Microsoft Active Accessibility selection. (IUIAutomationLegacyIAccessiblePattern.Select)
helpviewer_keywords: ["IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","Select method","IUIAutomationLegacyIAccessiblePattern.Select","IUIAutomationLegacyIAccessiblePattern::Select","Select","Select method [Windows Accessibility]","Select method [Windows Accessibility]","IUIAutomationLegacyIAccessiblePattern interface","uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_Select","uiauto_IUIAutomationLegacyIAccessiblePattern_Select","uiautomationclient/IUIAutomationLegacyIAccessiblePattern::Select","winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_Select"]
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_Select.htm
tech.root: WinAuto
ms.assetid: d311a10d-4762-47c9-a0bd-299da43827f7
ms.date: 12/05/2018
ms.keywords: IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],Select method, IUIAutomationLegacyIAccessiblePattern.Select, IUIAutomationLegacyIAccessiblePattern::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_Select, uiauto_IUIAutomationLegacyIAccessiblePattern_Select, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::Select, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_Select
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUIAutomationLegacyIAccessiblePattern::Select
 - uiautomationclient/IUIAutomationLegacyIAccessiblePattern::Select
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
 - IUIAutomationLegacyIAccessiblePattern.Select
---

# IUIAutomationLegacyIAccessiblePattern::Select


## -description

Performs a Microsoft Active Accessibility selection.

## -parameters

### -param flagsSelect

Type: <b>long</b>

Specifies which selection or focus operations are to be performed. This parameter must have a combination of the values described in <a href="/windows/desktop/WinAuto/selflag">SELFLAG Constants</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern">IUIAutomationLegacyIAccessiblePattern</a>

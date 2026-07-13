---
UID: NF:uiautomationclient.IUIAutomationTextEditPattern.GetActiveComposition
title: IUIAutomationTextEditPattern::GetActiveComposition (uiautomationclient.h)
description: Returns the active composition. (IUIAutomationTextEditPattern.GetActiveComposition)
helpviewer_keywords: ["GetActiveComposition","GetActiveComposition method [Windows Accessibility]","GetActiveComposition method [Windows Accessibility]","IUIAutomationTextEditPattern interface","IUIAutomationTextEditPattern interface [Windows Accessibility]","GetActiveComposition method","IUIAutomationTextEditPattern.GetActiveComposition","IUIAutomationTextEditPattern::GetActiveComposition","uiautomationclient/IUIAutomationTextEditPattern::GetActiveComposition","winauto.uiauto_IUIAutomationTextEditPattern_GetActiveComposition"]
old-location: winauto\uiauto_IUIAutomationTextEditPattern_GetActiveComposition.htm
tech.root: WinAuto
ms.assetid: F6503B77-19FB-6D00-D20C-E3D3F0EC28DA
ms.date: 12/05/2018
ms.keywords: GetActiveComposition, GetActiveComposition method [Windows Accessibility], GetActiveComposition method [Windows Accessibility],IUIAutomationTextEditPattern interface, IUIAutomationTextEditPattern interface [Windows Accessibility],GetActiveComposition method, IUIAutomationTextEditPattern.GetActiveComposition, IUIAutomationTextEditPattern::GetActiveComposition, uiautomationclient/IUIAutomationTextEditPattern::GetActiveComposition, winauto.uiauto_IUIAutomationTextEditPattern_GetActiveComposition
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IUIAutomationTextEditPattern::GetActiveComposition
 - uiautomationclient/IUIAutomationTextEditPattern::GetActiveComposition
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
 - IUIAutomationTextEditPattern.GetActiveComposition
---

# IUIAutomationTextEditPattern::GetActiveComposition


## -description

Returns the active composition.

## -parameters

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Pointer to the range of the current conversion (none if there is no conversion).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Active composition is relevant to Input Method Editors (IMEs).

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtexteditpattern">IUIAutomationTextEditPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>

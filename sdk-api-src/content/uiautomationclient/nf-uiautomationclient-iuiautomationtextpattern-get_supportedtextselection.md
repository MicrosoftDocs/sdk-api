---
UID: NF:uiautomationclient.IUIAutomationTextPattern.get_SupportedTextSelection
title: IUIAutomationTextPattern::get_SupportedTextSelection (uiautomationclient.h)
description: Retrieves a value that specifies the type of text selection that is supported by the control. (IUIAutomationTextPattern.get_SupportedTextSelection)
helpviewer_keywords: ["IUIAutomationTextPattern interface [Windows Accessibility]","SupportedTextSelection property","IUIAutomationTextPattern.SupportedTextSelection","IUIAutomationTextPattern.get_SupportedTextSelection","IUIAutomationTextPattern::SupportedTextSelection","IUIAutomationTextPattern::get_SupportedTextSelection","SupportedTextSelection property [Windows Accessibility]","SupportedTextSelection property [Windows Accessibility]","IUIAutomationTextPattern interface","get_SupportedTextSelection","uiauto.uiauto_IUIAutomationTextPattern_SupportedTextSelection","uiauto_IUIAutomationTextPattern_SupportedTextSelection","uiautomationclient/IUIAutomationTextPattern::SupportedTextSelection","uiautomationclient/IUIAutomationTextPattern::get_SupportedTextSelection","winauto.uiauto_IUIAutomationTextPattern_SupportedTextSelection"]
old-location: winauto\uiauto_IUIAutomationTextPattern_SupportedTextSelection.htm
tech.root: WinAuto
ms.assetid: 794c08d4-9305-4fdd-8ca0-188e1e9b6547
ms.date: 08/22/2023
ms.keywords: IUIAutomationTextPattern interface [Windows Accessibility],SupportedTextSelection property, IUIAutomationTextPattern.SupportedTextSelection, IUIAutomationTextPattern.get_SupportedTextSelection, IUIAutomationTextPattern::SupportedTextSelection, IUIAutomationTextPattern::get_SupportedTextSelection, SupportedTextSelection property [Windows Accessibility], SupportedTextSelection property [Windows Accessibility],IUIAutomationTextPattern interface, get_SupportedTextSelection, uiauto.uiauto_IUIAutomationTextPattern_SupportedTextSelection, uiauto_IUIAutomationTextPattern_SupportedTextSelection, uiautomationclient/IUIAutomationTextPattern::SupportedTextSelection, uiautomationclient/IUIAutomationTextPattern::get_SupportedTextSelection, winauto.uiauto_IUIAutomationTextPattern_SupportedTextSelection
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
 - IUIAutomationTextPattern::get_SupportedTextSelection
 - uiautomationclient/IUIAutomationTextPattern::get_SupportedTextSelection
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
 - IUIAutomationTextPattern.SupportedTextSelection
 - IUIAutomationTextPattern.get_SupportedTextSelection
---

# IUIAutomationTextPattern::get_SupportedTextSelection

## -description

Retrieves a value that specifies the type of text selection that is supported by the control.

This property is read-only.

## -parameters

### -param supportedTextSelection

Type: **[SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md)\***

When this function returns, contains a pointer to the [SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md) object.

## -returns

Type: **[HRESULT](/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also

[IUIAutomationTextPattern interface](nn-uiautomationclient-iuiautomationtextpattern.md), [UI Automation Support for Textual Content](/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview)

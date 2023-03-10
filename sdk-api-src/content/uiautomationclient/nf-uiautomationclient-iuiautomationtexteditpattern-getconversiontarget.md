---
UID: NF:uiautomationclient.IUIAutomationTextEditPattern.GetConversionTarget
title: IUIAutomationTextEditPattern::GetConversionTarget (uiautomationclient.h)
description: Returns the current conversion target range. (IUIAutomationTextEditPattern.GetConversionTarget)
helpviewer_keywords: ["GetConversionTarget","GetConversionTarget method [Windows Accessibility]","GetConversionTarget method [Windows Accessibility]","IUIAutomationTextEditPattern interface","IUIAutomationTextEditPattern interface [Windows Accessibility]","GetConversionTarget method","IUIAutomationTextEditPattern.GetConversionTarget","IUIAutomationTextEditPattern::GetConversionTarget","uiautomationclient/IUIAutomationTextEditPattern::GetConversionTarget","winauto.uiauto_IUIAutomationTextEditPattern_GetConversionTarget"]
old-location: winauto\uiauto_IUIAutomationTextEditPattern_GetConversionTarget.htm
tech.root: WinAuto
ms.assetid: C7471306-9D7F-5FE8-9A57-7A3ABB45B59F
ms.date: 12/05/2018
ms.keywords: GetConversionTarget, GetConversionTarget method [Windows Accessibility], GetConversionTarget method [Windows Accessibility],IUIAutomationTextEditPattern interface, IUIAutomationTextEditPattern interface [Windows Accessibility],GetConversionTarget method, IUIAutomationTextEditPattern.GetConversionTarget, IUIAutomationTextEditPattern::GetConversionTarget, uiautomationclient/IUIAutomationTextEditPattern::GetConversionTarget, winauto.uiauto_IUIAutomationTextEditPattern_GetConversionTarget
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
 - IUIAutomationTextEditPattern::GetConversionTarget
 - uiautomationclient/IUIAutomationTextEditPattern::GetConversionTarget
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
 - IUIAutomationTextEditPattern.GetConversionTarget
---

# IUIAutomationTextEditPattern::GetConversionTarget


## -description

Returns the current conversion target range.

## -parameters

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Pointer to the conversion target range (none if there is no conversion).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtexteditpattern">IUIAutomationTextEditPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>

---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetCachedSelection
title: IUIAutomationLegacyIAccessiblePattern::GetCachedSelection (uiautomationclient.h)
description: Retrieves the cached Microsoft Active Accessibility property that identifies the selected children of this element.
helpviewer_keywords: ["GetCachedSelection","GetCachedSelection method [Windows Accessibility]","GetCachedSelection method [Windows Accessibility]","IUIAutomationLegacyIAccessiblePattern interface","IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","GetCachedSelection method","IUIAutomationLegacyIAccessiblePattern.GetCachedSelection","IUIAutomationLegacyIAccessiblePattern::GetCachedSelection","uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection","uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection","uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCachedSelection","winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection"]
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection.htm
tech.root: WinAuto
ms.assetid: 923c3f64-7205-4d41-b726-90324e65661e
ms.date: 12/05/2018
ms.keywords: GetCachedSelection, GetCachedSelection method [Windows Accessibility], GetCachedSelection method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetCachedSelection method, IUIAutomationLegacyIAccessiblePattern.GetCachedSelection, IUIAutomationLegacyIAccessiblePattern::GetCachedSelection, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection, uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCachedSelection, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCachedSelection
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
 - IUIAutomationLegacyIAccessiblePattern::GetCachedSelection
 - uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCachedSelection
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
 - IUIAutomationLegacyIAccessiblePattern.GetCachedSelection
---

# IUIAutomationLegacyIAccessiblePattern::GetCachedSelection


## -description

Retrieves the cached Microsoft Active Accessibility property that identifies the selected children of this element.

## -parameters

### -param pvarSelectedChildren [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the cached collection of the selected child elements.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern">IUIAutomationLegacyIAccessiblePattern</a>
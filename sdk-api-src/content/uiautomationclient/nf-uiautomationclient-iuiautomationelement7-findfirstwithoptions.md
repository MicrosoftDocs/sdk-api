---
UID: NF:uiautomationclient.IUIAutomationElement7.FindFirstWithOptions
title: IUIAutomationElement7::FindFirstWithOptions (uiautomationclient.h)
description: Finds the first matching element in the specified order.
helpviewer_keywords: ["FindFirstWithOptions","FindFirstWithOptions method [Windows Accessibility]","FindFirstWithOptions method [Windows Accessibility]","IUIAutomationElement7 interface","IUIAutomationElement7 interface [Windows Accessibility]","FindFirstWithOptions method","IUIAutomationElement7.FindFirstWithOptions","IUIAutomationElement7::FindFirstWithOptions","uiautomationclient/IUIAutomationElement7::FindFirstWithOptions","winauto.uiauto_IUIAutomationElement7_FindFirstWithOptions","winauto.uiauto_iuiautomationelement_findfirstwithoptions"]
old-location: winauto\uiauto_IUIAutomationElement7_FindFirstWithOptions.htm
tech.root: WinAuto
ms.assetid: D6A872E7-290D-45E7-B4FD-7201A4E990A2
ms.date: 12/05/2018
ms.keywords: FindFirstWithOptions, FindFirstWithOptions method [Windows Accessibility], FindFirstWithOptions method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindFirstWithOptions method, IUIAutomationElement7.FindFirstWithOptions, IUIAutomationElement7::FindFirstWithOptions, uiautomationclient/IUIAutomationElement7::FindFirstWithOptions, winauto.uiauto_IUIAutomationElement7_FindFirstWithOptions, winauto.uiauto_iuiautomationelement_findfirstwithoptions
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IUIAutomationElement7::FindFirstWithOptions
 - uiautomationclient/IUIAutomationElement7::FindFirstWithOptions
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
 - IUIAutomationElement7.FindFirstWithOptions
---

# IUIAutomationElement7::FindFirstWithOptions


## -description

Finds the first matching element in the specified order.

## -parameters

### -param scope [in]

A combination of values specifying the scope of the search.

### -param condition [in]

A pointer to a condition that represents the criteria to match.

### -param traversalOptions

Enumeration value specifying the tree navigation order.

### -param root [in, optional]

A pointer to the element with which to begin the search.

### -param found [out, retval]

Receives a pointer to the element. <b>NULL</b> is returned if no matching element is found.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement7">IUIAutomationElement7</a>
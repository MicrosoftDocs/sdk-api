---
UID: NF:uiautomationclient.IUIAutomationElement7.FindAllWithOptions
title: IUIAutomationElement7::FindAllWithOptions (uiautomationclient.h)
description: Find all matching elements in the specified order.
helpviewer_keywords: ["FindAllWithOptions","FindAllWithOptions method [Windows Accessibility]","FindAllWithOptions method [Windows Accessibility]","IUIAutomationElement7 interface","IUIAutomationElement7 interface [Windows Accessibility]","FindAllWithOptions method","IUIAutomationElement7.FindAllWithOptions","IUIAutomationElement7::FindAllWithOptions","uiautomationclient/IUIAutomationElement7::FindAllWithOptions","winauto.uiauto_IUIAutomationElement7_FindAllWithOptions","winauto.uiauto_iuiautomationelement_findallwithoptions"]
old-location: winauto\uiauto_IUIAutomationElement7_FindAllWithOptions.htm
tech.root: WinAuto
ms.assetid: 1B157EBE-5576-41E8-9B4C-752EFA7832E5
ms.date: 12/05/2018
ms.keywords: FindAllWithOptions, FindAllWithOptions method [Windows Accessibility], FindAllWithOptions method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindAllWithOptions method, IUIAutomationElement7.FindAllWithOptions, IUIAutomationElement7::FindAllWithOptions, uiautomationclient/IUIAutomationElement7::FindAllWithOptions, winauto.uiauto_IUIAutomationElement7_FindAllWithOptions, winauto.uiauto_iuiautomationelement_findallwithoptions
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
 - IUIAutomationElement7::FindAllWithOptions
 - uiautomationclient/IUIAutomationElement7::FindAllWithOptions
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
 - IUIAutomationElement7.FindAllWithOptions
---

# IUIAutomationElement7::FindAllWithOptions


## -description

Find all matching elements in the specified order.

## -parameters

### -param scope

A combination of values specifying the scope of the search.

### -param condition [in]

A pointer to a condition that represents the criteria to match.

### -param traversalOptions

Enumeration value specifying the tree navigation order.

### -param root [in, optional]

A pointer to the element with which to begin the search.

### -param found [out]

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement7">IUIAutomationElement7</a>
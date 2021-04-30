---
UID: NF:uiautomationcoreapi.UiaRaiseChangesEvent
title: UiaRaiseChangesEvent function (uiautomationcoreapi.h)
description: Called by providers to notify the Microsoft UI Automation core that a change has occurred.
helpviewer_keywords: ["UiaRaiseChangesEvent","UiaRaiseChangesEvent function [Windows Accessibility]","uiautomationcoreapi/UiaRaiseChangesEvent","winauto.uiauto_UiaRaiseChangesEventFunction"]
old-location: winauto\uiauto_UiaRaiseChangesEventFunction.htm
tech.root: WinAuto
ms.assetid: AA6F1F6E-3EE9-44A6-B1AE-B08013DC1E37
ms.date: 12/05/2018
ms.keywords: UiaRaiseChangesEvent, UiaRaiseChangesEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseChangesEvent, winauto.uiauto_UiaRaiseChangesEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaRaiseChangesEvent
 - uiautomationcoreapi/UiaRaiseChangesEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseChangesEvent
---

# UiaRaiseChangesEvent function


## -description

Called by providers to notify the Microsoft UI Automation core that a change has occurred.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider node where the change event occurred.

### -param eventIdCount [in]

The number of changes that occurred. This is the number of <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiachangeinfo">UiaChangeInfo</a> structures pointed to by the <i>pUiaChanges</i> parameter.

### -param pUiaChanges [in]

A collection of pointers to <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiachangeinfo">UiaChangeInfo</a> structures.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

<a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> value indicating success or failure.
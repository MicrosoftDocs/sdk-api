---
UID: NF:uiautomationcoreapi.UiaRaiseActiveTextPositionChangedEvent
title: UiaRaiseActiveTextPositionChangedEvent function (uiautomationcoreapi.h)
description: Called by a provider to notify the Microsoft UI Automation core that a text control has programmatically changed text. (UiaRaiseActiveTextPositionChangedEvent)
helpviewer_keywords: ["UiaRaiseActiveTextPositionChangedEvent","UiaRaiseActiveTextPositionChangedEvent function [Windows Accessibility]","uiautomationcoreapi/UiaRaiseActiveTextPositionChangedEvent","winauto.uiauto_UiaRaiseActiveTextPositionChangedEventFunction"]
old-location: winauto\uiauto_UiaRaiseActiveTextPositionChangedEventFunction.htm
tech.root: WinAuto
ms.date: 09/24/2020
ms.keywords: UiaRaiseActiveTextPositionChangedEvent, UiaRaiseActiveTextPositionChangedEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseActiveTextPositionChangedEvent, winauto.uiauto_UiaRaiseActiveTextPositionChangedEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - UiaRaiseActiveTextPositionChangedEvent
 - uiautomationcoreapi/UiaRaiseActiveTextPositionChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseActiveTextPositionChangedEvent
---

# UiaRaiseActiveTextPositionChangedEvent function

## -description

Called by a provider to notify the Microsoft UI Automation core that the position within a text control has programmatically changed.

## -parameters

### -param provider [in]

Type: <b><a href="/windows/win32/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider node where the position change within the text occurred.

### -param textRange [in, optional]

Type: <b><a href="/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>*</b>

The text range change that occurred, if applicable.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

## -see-also

[IUIAutomation6::AddActiveTextPositionChangedEventHandler](../uiautomationclient/nf-uiautomationclient-iuiautomation6-addactivetextpositionchangedeventhandler.md), [IUIAutomation6::RemoveActiveTextPositionChangedEventHandler](../uiautomationclient/nf-uiautomationclient-iuiautomation6-removeactivetextpositionchangedeventhandler.md), [IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler](../uiautomationclient/nf-uiautomationclient-iuiautomationeventhandlergroup-addactivetextpositionchangedeventhandler.md)

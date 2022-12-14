---
UID: NE:uiribbon.UI_EVENTLOCATION
title: UI_EVENTLOCATION (uiribbon.h)
description: Identifies the locations where events associated with a Ribbon control can originate.
helpviewer_keywords: ["UI_EVENTLOCATION","UI_EVENTLOCATION enumeration [Windows Ribbon]","UI_EVENTLOCATION_ApplicationMenu","UI_EVENTLOCATION_ContextPopup","UI_EVENTLOCATION_QAT","UI_EVENTLOCATION_Ribbon","uiribbon/UI_EVENTLOCATION","uiribbon/UI_EVENTLOCATION_ApplicationMenu","uiribbon/UI_EVENTLOCATION_ContextPopup","uiribbon/UI_EVENTLOCATION_QAT","uiribbon/UI_EVENTLOCATION_Ribbon","windowsribbon.ui_eventlocation"]
old-location: windowsribbon\ui_eventlocation.htm
tech.root: windowsribbon
ms.assetid: EA278262-8CA7-42A3-9F66-0C7B4D3AA525
ms.date: 12/05/2018
ms.keywords: UI_EVENTLOCATION, UI_EVENTLOCATION enumeration [Windows Ribbon], UI_EVENTLOCATION_ApplicationMenu, UI_EVENTLOCATION_ContextPopup, UI_EVENTLOCATION_QAT, UI_EVENTLOCATION_Ribbon, uiribbon/UI_EVENTLOCATION, uiribbon/UI_EVENTLOCATION_ApplicationMenu, uiribbon/UI_EVENTLOCATION_ContextPopup, uiribbon/UI_EVENTLOCATION_QAT, uiribbon/UI_EVENTLOCATION_Ribbon, windowsribbon.ui_eventlocation
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_EVENTLOCATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_EVENTLOCATION
 - uiribbon/UI_EVENTLOCATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EVENTLOCATION
---

# UI_EVENTLOCATION enumeration


## -description

Identifies the locations where events associated with a Ribbon control can originate.

## -enum-fields

### -field UI_EVENTLOCATION_Ribbon:0

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-ribbon">Ribbon</a>.

### -field UI_EVENTLOCATION_QAT:1

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-quickaccesstoolbar">QuickAccessToolbar</a>.

### -field UI_EVENTLOCATION_ApplicationMenu:2

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-applicationmenu">ApplicationMenu</a>.

### -field UI_EVENTLOCATION_ContextPopup:3

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextpopup">ContextPopup</a>.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuieventlogger-onuievent">OnUIEvent</a>



<a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_eventtype">UI_EVENTTYPE</a>

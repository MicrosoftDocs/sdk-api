---
UID: NE:uiautomationcore.ActiveEnd
title: ActiveEnd (uiautomationcore.h)
description: Contains possible values for the SelectionActiveEnd text attribute, which indicates the location of the caret relative to a text range that represents the currently selected text.
helpviewer_keywords: ["ActiveEnd","ActiveEnd enumeration [Windows Accessibility]","ActiveEnd_End","ActiveEnd_None","ActiveEnd_Start","uiautomationcore/ActiveEnd","uiautomationcore/ActiveEnd_End","uiautomationcore/ActiveEnd_None","uiautomationcore/ActiveEnd_Start","winauto.uiauto_ActiveEnd"]
old-location: winauto\uiauto_ActiveEnd.htm
tech.root: WinAuto
ms.assetid: 20A6813A-FA1B-43BD-A2D2-AF9AB5A7CC99
ms.date: 12/05/2018
ms.keywords: ActiveEnd, ActiveEnd enumeration [Windows Accessibility], ActiveEnd_End, ActiveEnd_None, ActiveEnd_Start, uiautomationcore/ActiveEnd, uiautomationcore/ActiveEnd_End, uiautomationcore/ActiveEnd_None, uiautomationcore/ActiveEnd_Start, winauto.uiauto_ActiveEnd
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ActiveEnd
 - uiautomationcore/ActiveEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - ActiveEnd
---

# ActiveEnd enumeration


## -description

Contains possible values for the <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">SelectionActiveEnd</a> text attribute, which indicates the location of the caret relative to a text range that represents the currently selected text.

## -enum-fields

### -field ActiveEnd_None:0

The caret is not at either end of the text range.

### -field ActiveEnd_Start:1

The caret is at the beginning of the text range.

### -field ActiveEnd_End:2

The caret is at the end of the text range.

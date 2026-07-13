---
UID: NE:uiribbon.UI_CONTROLDOCK
title: UI_CONTROLDOCK (uiribbon.h)
description: Specifies values that identify the dock state of the Quick Access Toolbar (QAT).
helpviewer_keywords: ["UI_CONTROLDOCK","UI_CONTROLDOCK enumeration [Windows Ribbon]","UI_CONTROLDOCK_BOTTOM","UI_CONTROLDOCK_TOP","scenicintent_UI_CONTROLDOCK","uiribbon/UI_CONTROLDOCK","uiribbon/UI_CONTROLDOCK_BOTTOM","uiribbon/UI_CONTROLDOCK_TOP","windowsribbon.windowsribbon_ui_controldock"]
old-location: windowsribbon\windowsribbon_ui_controldock.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_controldock.htm
ms.date: 12/05/2018
ms.keywords: UI_CONTROLDOCK, UI_CONTROLDOCK enumeration [Windows Ribbon], UI_CONTROLDOCK_BOTTOM, UI_CONTROLDOCK_TOP, scenicintent_UI_CONTROLDOCK, uiribbon/UI_CONTROLDOCK, uiribbon/UI_CONTROLDOCK_BOTTOM, uiribbon/UI_CONTROLDOCK_TOP, windowsribbon.windowsribbon_ui_controldock
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_CONTROLDOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_CONTROLDOCK
 - uiribbon/UI_CONTROLDOCK
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
 - UI_CONTROLDOCK
---

# UI_CONTROLDOCK enumeration


## -description

Specifies values that identify the dock state of the Quick Access Toolbar (QAT).

## -enum-fields

### -field UI_CONTROLDOCK_TOP:1

The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.

<img alt="Screen shot showing the Quick Access Toolbar docked above the Ribbon in the nonclient area." src="./images/QAT_DockTop.png"/>

### -field UI_CONTROLDOCK_BOTTOM:3

The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.

<img alt="Screen shot showing the Quick Access Toolbar docked below the Ribbon." src="./images/QAT_DockBottom.png"/>

## -remarks

The QAT dock position is based on the <b>UI_CONTROLDOCK</b> value in <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-quickaccesstoolbardock">UI_PKEY_QuickAccessToolbarDock</a>.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-quickaccesstoolbardock">UI_PKEY_QuickAccessToolbarDock</a>

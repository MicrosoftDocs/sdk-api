---
UID: NS:msime._IMEDLG
title: IMEDLG (msime.h)
description: Used when invoking the Microsoft IME's Dictionary Tool or Word Register Dialog Window from the app.
helpviewer_keywords: ["IMEDLG","IMEDLG structure [Internationalization for Windows Applications]","PIMEDLG","PIMEDLG structure pointer [Internationalization for Windows Applications]","intl.imedlg","msime/IMEDLG","msime/PIMEDLG"]
old-location: intl\imedlg.htm
tech.root: Intl
ms.assetid: 14F39582-F51D-456F-BC19-AFE6E50D4155
ms.date: 12/05/2018
ms.keywords: IMEDLG, IMEDLG structure [Internationalization for Windows Applications], PIMEDLG, PIMEDLG structure pointer [Internationalization for Windows Applications], intl.imedlg, msime/IMEDLG, msime/PIMEDLG
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMEDLG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMEDLG
 - msime/_IMEDLG
 - IMEDLG
 - msime/IMEDLG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMEDLG
---

# IMEDLG structure


## -description

Used when invoking the Microsoft IME's Dictionary Tool or Word Register Dialog Window from the app.

## -struct-fields

### -field cbIMEDLG

The size of this structure. You must set this value before using the structure.

### -field hwnd

The parent window handle of the Register Word Dialog.

### -field lpwstrWord

<b>NULL</b>, or  the string to be registered. It shows in the Word Register Dialog's "Display" field.

### -field nTabId

The initial tab ID, 0 or 1.

## -see-also

<a href="/windows/desktop/api/msime/nf-msime-ifecommon-invokedicttooldialog">IFECommon::InvokeDictToolDialog</a>



<a href="/windows/desktop/api/msime/nf-msime-ifecommon-invokewordregdialog">IFECommon::InvokeWordRegDialog</a>
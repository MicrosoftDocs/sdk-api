---
UID: NF:oledlg.OleUIAddVerbMenuW
title: OleUIAddVerbMenuW function (oledlg.h)
description: Adds the Verb menu for the specified object to the specified menu. (Unicode)
helpviewer_keywords: ["OleUIAddVerbMenu", "OleUIAddVerbMenu function [COM]", "OleUIAddVerbMenuW", "_ole_OleUIAddVerbMenu", "com.oleuiaddverbmenu", "oledlg/OleUIAddVerbMenu", "oledlg/OleUIAddVerbMenuW"]
old-location: com\oleuiaddverbmenu.htm
tech.root: com
ms.assetid: 6efb49e7-b3c1-4035-892d-4572db47b951
ms.date: 12/05/2018
ms.keywords: OleUIAddVerbMenu, OleUIAddVerbMenu function [COM], OleUIAddVerbMenuA, OleUIAddVerbMenuW, _ole_OleUIAddVerbMenu, com.oleuiaddverbmenu, oledlg/OleUIAddVerbMenu, oledlg/OleUIAddVerbMenuA, oledlg/OleUIAddVerbMenuW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIAddVerbMenuW (Unicode) and OleUIAddVerbMenuA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleUIAddVerbMenuW
 - oledlg/OleUIAddVerbMenuW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUIAddVerbMenu
 - OleUIAddVerbMenuA
 - OleUIAddVerbMenuW
---

# OleUIAddVerbMenuW function


## -description

Adds the <b>Verb</b> menu for the specified object to the specified menu.

## -parameters

### -param lpOleObj [in, optional]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface on the selected object. If this is <b>NULL</b>, then a default disabled menu item is created.

### -param lpszShortType [in, optional]

Pointer to the short name defined in the registry (AuxName==2) for the object identified with <i>lpOleObj</i>. If the string is not known, then <b>NULL</b> may be passed. If <b>NULL</b> is passed, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a> is called to retrieve it. If the caller has easy access to the string, it is faster to pass it in.

### -param hMenu [in]

Handle to the menu in which to make modifications.

### -param uPos [in]

Position of the menu item.

### -param uIDVerbMin [in]

The identifier value at which to start the verbs.

### -param uIDVerbMax [in]

 The maximum identifier value to be used for object verbs. If <i>uIDVerbMax</i> is 0, then no maximum identifier value is used.

### -param bAddConvert [in]

 Indicates whether to add a <b>Convert</b> item to the bottom of the menu (preceded by a separator).

### -param idConvert [in]

The identifier value to use for the <b>Convert</b> menu item, if <i>bAddConvert</i> is <b>TRUE</b>.

### -param lphMenu [out]

An <b>HMENU</b> pointer to the cascading verb menu if it's created. If there is only one verb, this will be filled with <b>NULL</b>.

## -returns

This function returns <b>TRUE</b> if <i>lpOleObj</i> was valid and at least one verb was added to the menu. A <b>FALSE</b> return indicates that <i>lpOleObj</i> was <b>NULL</b> and a disabled default menu item was created.

## -remarks

If the object has one verb, the verb is added directly to the given menu.





> [!NOTE]
> The oledlg.h header defines OleUIAddVerbMenu as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

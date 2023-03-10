---
UID: NE:prntvpt.tagEDefaultDevmodeType
title: EDefaultDevmodeType (prntvpt.h)
description: Enables users to specify which DEVMODE to use as the source of default values when a print ticket does not specify all possible settings.
helpviewer_keywords: ["EDefaultDevmodeType","EDefaultDevmodeType enumeration [Windows GDI]","_win32_EDefaultDevmodeType","gdi.edefaultdevmodetype","kPrinterDefaultDevmode","kUserDefaultDevmode","prntvpt/EDefaultDevmodeType","prntvpt/kPrinterDefaultDevmode","prntvpt/kUserDefaultDevmode"]
old-location: gdi\edefaultdevmodetype.htm
tech.root: xps
ms.assetid: f3144ff6-1228-4e17-b118-fe70136edeea
ms.date: 12/05/2018
ms.keywords: EDefaultDevmodeType, EDefaultDevmodeType enumeration [Windows GDI], _win32_EDefaultDevmodeType, gdi.edefaultdevmodetype, kPrinterDefaultDevmode, kUserDefaultDevmode, prntvpt/EDefaultDevmodeType, prntvpt/kPrinterDefaultDevmode, prntvpt/kUserDefaultDevmode
req.header: prntvpt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: EDefaultDevmodeType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEDefaultDevmodeType
 - prntvpt/tagEDefaultDevmodeType
 - EDefaultDevmodeType
 - prntvpt/EDefaultDevmodeType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - prntvpt.h
api_name:
 - EDefaultDevmodeType
---

# EDefaultDevmodeType enumeration


## -description

Enables users to specify which <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> to use as the source of default values when a print ticket does not specify all possible settings.

## -enum-fields

### -field kUserDefaultDevmode

The user's default preferences.

### -field kPrinterDefaultDevmode

The print queue's default preferences.

## -remarks

If user defaults are not available when using kUserDefaultDevmode, queue defaults will be used.


---
UID: NE:prntvpt.tagEDefaultDevmodeType
title: EDefaultDevmodeType (prntvpt.h)
author: windows-sdk-content
description: Enables users to specify which DEVMODE to use as the source of default values when a print ticket does not specify all possible settings.
old-location: gdi\edefaultdevmodetype.htm
tech.root: printdocs
ms.assetid: f3144ff6-1228-4e17-b118-fe70136edeea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EDefaultDevmodeType, EDefaultDevmodeType enumeration [Windows GDI], _win32_EDefaultDevmodeType, gdi.edefaultdevmodetype, kPrinterDefaultDevmode, kUserDefaultDevmode, prntvpt/EDefaultDevmodeType, prntvpt/kPrinterDefaultDevmode, prntvpt/kUserDefaultDevmode
ms.topic: enum
f1_keywords: 
 - "prntvpt/EDefaultDevmodeType"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - prntvpt.h
api_name:
 - EDefaultDevmodeType
product: Windows
targetos: Windows
req.typenames: EDefaultDevmodeType
req.redist: 
ms.custom: 19H1
---

# EDefaultDevmodeType enumeration


## -description


Enables users to specify which <a href="https://docs.microsoft.com/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> to use as the source of default values when a print ticket does not specify all possible settings.


## -enum-fields




### -field kUserDefaultDevmode

The user's default preferences.


### -field kPrinterDefaultDevmode

The print queue's default preferences.


## -remarks



If user defaults are not available when using kUserDefaultDevmode, queue defaults will be used.




---
UID: NE:prntvpt.tagEDefaultDevmodeType
title: tagEDefaultDevmodeType
author: windows-sdk-content
description: Enables users to specify which DEVMODE to use as the source of default values when a print ticket does not specify all possible settings.
old-location: gdi\edefaultdevmodetype.htm
tech.root: printdocs
ms.assetid: f3144ff6-1228-4e17-b118-fe70136edeea
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EDefaultDevmodeType, EDefaultDevmodeType enumeration [Windows GDI], _win32_EDefaultDevmodeType, gdi.edefaultdevmodetype, kPrinterDefaultDevmode, kUserDefaultDevmode, prntvpt/EDefaultDevmodeType, prntvpt/kPrinterDefaultDevmode, prntvpt/kUserDefaultDevmode, tagEDefaultDevmodeType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
---

# tagEDefaultDevmodeType enumeration


## -description


Enables users to specify which <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> to use as the source of default values when a print ticket does not specify all possible settings.


## -enum-fields




### -field kUserDefaultDevmode

The user's default preferences.


### -field kPrinterDefaultDevmode

The print queue's default preferences.


## -remarks



If user defaults are not available when using kUserDefaultDevmode, queue defaults will be used.




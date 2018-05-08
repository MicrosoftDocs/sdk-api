---
UID: NS:shellapi._OPEN_PRINTER_PROPS_INFOW
title: "_OPEN_PRINTER_PROPS_INFOW"
author: windows-driver-content
description: Identifies a particular property sheet in a printer's property pages and whether that property sheet should be modal. Optionally used with the SHInvokePrinterCommand function.
old-location: shell\OPEN_PRINTER_PROPS_INFO.htm
old-project: shell
ms.assetid: c5cabb04-20a2-40ce-aa4d-180b73db8eac
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: "*POPEN_PRINTER_PROPS_INFOW, OPEN_PRINTER_PROPS_INFO, OPEN_PRINTER_PROPS_INFO structure [Windows Shell], OPEN_PRINTER_PROPS_INFOA, OPEN_PRINTER_PROPS_INFOW, POPEN_PRINTER_PROPS_INFO, POPEN_PRINTER_PROPS_INFO structure pointer [Windows Shell], _OPEN_PRINTER_PROPS_INFOW, _shell_OPEN_PRINTER_PROPS_INFO, shell.OPEN_PRINTER_PROPS_INFO, shellapi/OPEN_PRINTER_PROPS_INFO, shellapi/OPEN_PRINTER_PROPS_INFOA, shellapi/OPEN_PRINTER_PROPS_INFOW, shellapi/POPEN_PRINTER_PROPS_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPEN_PRINTER_PROPS_INFOW (Unicode) and OPEN_PRINTER_PROPS_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OPEN_PRINTER_PROPS_INFOW, *POPEN_PRINTER_PROPS_INFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shellapi.h
api_name:
-	OPEN_PRINTER_PROPS_INFO
-	OPEN_PRINTER_PROPS_INFOA
-	OPEN_PRINTER_PROPS_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _OPEN_PRINTER_PROPS_INFOW structure


## -description


Identifies a particular property sheet in a printer's property pages and whether that property sheet should be modal. Optionally used with the <a href="https://msdn.microsoft.com/32a5802f-cef7-4dbd-affd-82285fe97a8c">SHInvokePrinterCommand</a> function.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of the structure.


### -field pszSheetName

Type: <b>LPSTR</b>

The name of the property sheet. If the specified sheet is not found, the property sheet still appears with the default first page.


### -field uSheetIndex

Type: <b>UINT</b>

The index of the property sheet in the array of property sheets that makes up the window. If empty or invalid, the default first page is displayed.


### -field dwFlags

Type: <b>DWORD</b>

Not used.


### -field bModal

Type: <b>BOOL</b>

<b>TRUE</b> if the property sheet should be modal; otherwise, <b>FALSE</b>.


## -remarks



This structure can be passed in the <i>lpBuf2</i> parameter of the <a href="https://msdn.microsoft.com/32a5802f-cef7-4dbd-affd-82285fe97a8c">SHInvokePrinterCommand</a> function when that function's <i>uAction</i> parameter is set to PRINTACTION_PROPERTIES.




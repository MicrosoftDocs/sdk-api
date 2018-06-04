---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _OPEN_PRINTER_PROPS_INFOA structure


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




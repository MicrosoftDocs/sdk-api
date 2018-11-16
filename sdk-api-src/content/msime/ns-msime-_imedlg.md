---
UID: NS:msime._IMEDLG
title: "_IMEDLG"
author: windows-sdk-content
description: Used when invoking the Microsoft IME's Dictionary Tool or Word Register Dialog Window from the app.
old-location: intl\imedlg.htm
tech.root: Intl
ms.assetid: 14F39582-F51D-456F-BC19-AFE6E50D4155
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMEDLG, IMEDLG structure [Internationalization for Windows Applications], PIMEDLG, PIMEDLG structure pointer [Internationalization for Windows Applications], _IMEDLG, intl.imedlg, msime/IMEDLG, msime/PIMEDLG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMEDLG
product: Windows
targetos: Windows
req.typenames: IMEDLG
req.redist: 
---

# _IMEDLG structure


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




<a href="https://msdn.microsoft.com/E70E3B78-58D7-40E9-8DAB-447B4CBC13F4">IFECommon::InvokeDictToolDialog</a>



<a href="https://msdn.microsoft.com/FBD09E98-9C89-4CE4-9D17-A13E2BE0AB91">IFECommon::InvokeWordRegDialog</a>
 

 


---
UID: NS:winuser.tagALTTABINFO
title: tagALTTABINFO
author: windows-sdk-content
description: Contains status information for the application-switching (ALT+TAB) window.
old-location: winmsg\alttabinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\alttabinfo.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPALTTABINFO, *PALTTABINFO, ALTTABINFO, ALTTABINFO structure [Windows and Messages], LPALTTABINFO, LPALTTABINFO structure pointer [Windows and Messages], PALTTABINFO, PALTTABINFO structure pointer [Windows and Messages], _win32_ALTTABINFO_str, _win32_alttabinfo_str_cpp, tagALTTABINFO, winmsg.alttabinfo, winui._win32_alttabinfo_str, winuser/ALTTABINFO, winuser/LPALTTABINFO, winuser/PALTTABINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
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
 - Winuser.h
api_name:
 - ALTTABINFO
product: Windows
targetos: Windows
req.typenames: ALTTABINFO, *PALTTABINFO, *LPALTTABINFO
req.redist: 
---

# tagALTTABINFO structure


## -description


Contains status information for the application-switching (ALT+TAB) window.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the structure. The caller must set this to <code>sizeof(ALTTABINFO)</code>. 


### -field cItems

Type: <b>int</b>

The number of items in the window. 


### -field cColumns

Type: <b>int</b>

The number of columns in the window. 


### -field cRows

Type: <b>int</b>

The number of rows in the window. 


### -field iColFocus

Type: <b>int</b>

The column of the item that has the focus. 


### -field iRowFocus

Type: <b>int</b>

The row of the item that has the focus. 


### -field cxItem

Type: <b>int</b>

The width of each icon in the application-switching window. 


### -field cyItem

Type: <b>int</b>

The height of each icon in the application-switching window. 


### -field ptStart

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The top-left corner of the first icon. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ff708599-50ad-4c5c-bc6c-532f1e9e730c">GetAltTabInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 


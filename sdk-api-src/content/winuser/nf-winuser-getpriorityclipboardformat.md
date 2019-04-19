---
UID: NF:winuser.GetPriorityClipboardFormat
title: GetPriorityClipboardFormat function (winuser.h)
author: windows-sdk-content
description: Retrieves the first available clipboard format in the specified list.
old-location: dataxchg\getpriorityclipboardformat.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getpriorityclipboardformat.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPriorityClipboardFormat, GetPriorityClipboardFormat function [Data Exchange], _win32_GetPriorityClipboardFormat, _win32_getpriorityclipboardformat_cpp, dataxchg.getpriorityclipboardformat, winui._win32_getpriorityclipboardformat, winuser/GetPriorityClipboardFormat
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetPriorityClipboardFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetPriorityClipboardFormat function


## -description


Retrieves the first available clipboard format in the specified list.


## -parameters




### -param paFormatPriorityList [in]

Type: <b>UINT*</b>

The clipboard formats, in priority order. For a description of the standard clipboard formats, see <a href="https://msdn.microsoft.com/f0af4e61-7ef1-4263-b2c5-e4114515124f">Standard Clipboard Formats</a> .


### -param cFormats [in]

Type: <b>int</b>

The number of entries in the 
     <i>paFormatPriorityList</i> array. This value must not be greater than the number of entries in the list.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the first clipboard format in the list for which data is available. If the clipboard is empty, the return value is NULL. If the clipboard contains data, but not in any of the specified formats, the return value is –1. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649036(v=VS.85).aspx">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649038(v=VS.85).aspx">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649040(v=VS.85).aspx">GetClipboardFormatName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649047(v=VS.85).aspx">IsClipboardFormatAvailable</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649049(v=VS.85).aspx">RegisterClipboardFormat</a>
 

 


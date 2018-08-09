---
UID: NF:winuser.GetPriorityClipboardFormat
title: GetPriorityClipboardFormat function
author: windows-sdk-content
description: Retrieves the first available clipboard format in the specified list.
old-location: dataxchg\getpriorityclipboardformat.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getpriorityclipboardformat.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPriorityClipboardFormat, GetPriorityClipboardFormat function [Data Exchange], _win32_GetPriorityClipboardFormat, _win32_getpriorityclipboardformat_cpp, dataxchg.getpriorityclipboardformat, winui._win32_getpriorityclipboardformat, winuser/GetPriorityClipboardFormat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3f9390f0-0fcb-4654-add0-eeea8f79b3f5">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/eca6e3ca-46d1-4f1d-a13c-63542e8eb8bf">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/58cb43df-32a5-44ed-b017-441fe18ce54b">GetClipboardFormatName</a>



<a href="https://msdn.microsoft.com/e1b6c3ff-9a39-4703-b096-8ab07c14db2d">IsClipboardFormatAvailable</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a>
 

 


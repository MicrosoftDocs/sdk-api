---
UID: NF:winuser.RegisterClipboardFormatA
title: RegisterClipboardFormatA function
author: windows-sdk-content
description: Registers a new clipboard format. This format can then be used as a valid clipboard format.
old-location: dataxchg\registerclipboardformat.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\registerclipboardformat.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: RegisterClipboardFormat, RegisterClipboardFormat function [Data Exchange], RegisterClipboardFormatA, RegisterClipboardFormatW, _win32_RegisterClipboardFormat, _win32_registerclipboardformat_cpp, dataxchg.registerclipboardformat, winui._win32_registerclipboardformat, winuser/RegisterClipboardFormat, winuser/RegisterClipboardFormatA, winuser/RegisterClipboardFormatW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterClipboardFormatW (Unicode) and RegisterClipboardFormatA (ANSI)
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
 - API-MS-Win-RTCore-NTUser-clipboard-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - api-ms-win-ntuser-ie-clipboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - RegisterClipboardFormat
 - RegisterClipboardFormatA
 - RegisterClipboardFormatW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterClipboardFormatA function


## -description


Registers a new clipboard format. This format can then be used as a valid clipboard format. 


## -parameters




### -param lpszFormat [in]

Type: <b>LPCTSTR</b>

The name of the new format. 


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value identifies the registered clipboard format.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If a registered format with the specified name already exists, a new format is not registered and the return value identifies the existing format. This enables more than one application to copy and paste data using the same registered clipboard format. Note that the format name comparison is case-insensitive.

Registered clipboard formats are identified by values in the range 0xC000 through 0xFFFF. 

When registered clipboard formats are placed on or retrieved from the clipboard, they must be in the form of an 
				<b>HGLOBAL</b> value. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms649016(v=VS.85).aspx">Registering a Clipboard Format</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649036(v=VS.85).aspx">CountClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649038(v=VS.85).aspx">EnumClipboardFormats</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649040(v=VS.85).aspx">GetClipboardFormatName</a>



<b>Reference</b>
 

 


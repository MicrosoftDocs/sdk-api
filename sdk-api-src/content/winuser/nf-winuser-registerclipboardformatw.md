---
UID: NF:winuser.RegisterClipboardFormatW
title: RegisterClipboardFormatW function (winuser.h)
description: Registers a new clipboard format. This format can then be used as a valid clipboard format. (Unicode)
helpviewer_keywords: ["RegisterClipboardFormat", "RegisterClipboardFormat function [Data Exchange]", "RegisterClipboardFormatW", "_win32_RegisterClipboardFormat", "_win32_registerclipboardformat_cpp", "dataxchg.registerclipboardformat", "winui._win32_registerclipboardformat", "winuser/RegisterClipboardFormat", "winuser/RegisterClipboardFormatW"]
old-location: dataxchg\registerclipboardformat.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\registerclipboardformat.htm
ms.date: 12/05/2018
ms.keywords: RegisterClipboardFormat, RegisterClipboardFormat function [Data Exchange], RegisterClipboardFormatA, RegisterClipboardFormatW, _win32_RegisterClipboardFormat, _win32_registerclipboardformat_cpp, dataxchg.registerclipboardformat, winui._win32_registerclipboardformat, winuser/RegisterClipboardFormat, winuser/RegisterClipboardFormatA, winuser/RegisterClipboardFormatW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterClipboardFormatW
 - winuser/RegisterClipboardFormatW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-misc-l1-1-0.dll
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
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
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# RegisterClipboardFormatW function


## -description

Registers a new clipboard format. This format can then be used as a valid clipboard format.

## -parameters

### -param lpszFormat [in]

Type: <b>LPCTSTR</b>

The name of the new format.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value identifies the registered clipboard format.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a registered format with the specified name already exists, a new format is not registered and the return value identifies the existing format. This enables more than one application to copy and paste data using the same registered clipboard format. Note that the format name comparison is case-insensitive.

Registered clipboard formats are identified by values in the range 0xC000 through 0xFFFF. 

When registered clipboard formats are placed on or retrieved from the clipboard, they must be in the form of an 
				<b>HGLOBAL</b> value. 


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Registering a Clipboard Format</a>. 



<div class="code"></div>




> [!NOTE]
> The winuser.h header defines RegisterClipboardFormat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-countclipboardformats">CountClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardformatnamea">GetClipboardFormatName</a>



<b>Reference</b>

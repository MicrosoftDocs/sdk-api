---
UID: NF:winuser.GetClipboardFormatNameA
title: GetClipboardFormatNameA function (winuser.h)
description: Retrieves from the clipboard the name of the specified registered format. The function copies the name to the specified buffer. (ANSI)
helpviewer_keywords: ["GetClipboardFormatNameA", "winuser/GetClipboardFormatNameA"]
old-location: dataxchg\getclipboardformatname.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getclipboardformatname.htm
ms.date: 12/05/2018
ms.keywords: GetClipboardFormatName, GetClipboardFormatName function [Data Exchange], GetClipboardFormatNameA, GetClipboardFormatNameW, _win32_GetClipboardFormatName, _win32_getclipboardformatname_cpp, dataxchg.getclipboardformatname, winui._win32_getclipboardformatname, winuser/GetClipboardFormatName, winuser/GetClipboardFormatNameA, winuser/GetClipboardFormatNameW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetClipboardFormatNameW (Unicode) and GetClipboardFormatNameA (ANSI)
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
 - GetClipboardFormatNameA
 - winuser/GetClipboardFormatNameA
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
 - GetClipboardFormatName
 - GetClipboardFormatNameA
 - GetClipboardFormatNameW
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# GetClipboardFormatNameA function


## -description

Retrieves from the clipboard the name of the specified registered format. The function copies the name to the specified buffer.

## -parameters

### -param format [in]

Type: <b>UINT</b>

The type of format to be retrieved. This parameter must not specify any of the predefined clipboard formats.

### -param lpszFormatName [out]

Type: <b>LPTSTR</b>

The buffer that is to receive the format name.

### -param cchMaxCount [in]

Type: <b>int</b>

The maximum length, in 
					characters, of the string to be copied to the buffer. If the name exceeds this limit, it is truncated.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the length, in 
						characters, of the string copied to the buffer.

If the function fails, the return value is zero, indicating that the requested format does not exist or is predefined. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<h3><a id="Security_Considerations"></a><a id="security_considerations"></a><a id="SECURITY_CONSIDERATIONS"></a>Security Considerations</h3>
Using this function incorrectly might compromise the security of your program. For example, miscalculating the proper size of the <i>lpszFormatName</i> buffer, especially when the application is used in both ANSI and Unicode versions, can cause a buffer overflow. Also, note that the string is truncated if it is longer than the <i>cchMaxCount</i> parameter, which can lead to loss of information.


#### Examples

For an example, see <a href="/windows/desktop/dataxchg/using-the-clipboard">Example of a Clipboard Viewer</a>. 

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines GetClipboardFormatName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumclipboardformats">EnumClipboardFormats</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a>

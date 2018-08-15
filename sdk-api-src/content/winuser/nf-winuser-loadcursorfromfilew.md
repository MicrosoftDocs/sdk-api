---
UID: NF:winuser.LoadCursorFromFileW
title: LoadCursorFromFileW function
author: windows-sdk-content
description: Creates a cursor based on data contained in a file.
old-location: menurc\loadcursorfromfile.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursorfromfile.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LoadCursorFromFile, LoadCursorFromFile function [Menus and Other Resources], LoadCursorFromFileA, LoadCursorFromFileW, _win32_LoadCursorFromFile, _win32_loadcursorfromfile_cpp, menurc.loadcursorfromfile, winui._win32_loadcursorfromfile, winuser/LoadCursorFromFile, winuser/LoadCursorFromFileA, winuser/LoadCursorFromFileW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadCursorFromFileW (Unicode) and LoadCursorFromFileA (ANSI)
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
api_name:
 - LoadCursorFromFile
 - LoadCursorFromFileA
 - LoadCursorFromFileW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadCursorFromFileW function


## -description


Creates a cursor based on data contained in a file. 


## -parameters




### -param lpFileName [in]

Type: <b>LPCTSTR</b>

The source of the file data to be used to create the cursor. The data in the file must be in either .CUR or .ANI format.

If the high-order word of <i>lpFileName</i> is nonzero, it is a pointer to a string that is a fully qualified name of a file containing cursor data. 


## -returns



Type: <b>HCURSOR</b>

If the function is successful, the return value is a handle to the new cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 
						<b>GetLastError</b> may return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified file cannot be found.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648395(v=VS.85).aspx">SetSystemCursor</a>
 

 


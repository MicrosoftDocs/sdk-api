---
UID: NF:winuser.LoadCursorFromFileA
title: LoadCursorFromFileA function
author: windows-sdk-content
description: Creates a cursor based on data contained in a file.
old-location: menurc\loadcursorfromfile.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\loadcursorfromfile.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LoadCursorFromFile, LoadCursorFromFile function [Menus and Other Resources], LoadCursorFromFileA, LoadCursorFromFileW, _win32_LoadCursorFromFile, _win32_loadcursorfromfile_cpp, menurc.loadcursorfromfile, winui._win32_loadcursorfromfile, winuser/LoadCursorFromFile, winuser/LoadCursorFromFileA, winuser/LoadCursorFromFileW
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
req.unicode-ansi: LoadCursorFromFileW (Unicode) and LoadCursorFromFileA (ANSI)
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
api_name:
 - LoadCursorFromFile
 - LoadCursorFromFileA
 - LoadCursorFromFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadCursorFromFileA function


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



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/59b14556-34b9-4de3-843b-83d72daca128">SetSystemCursor</a>
 

 


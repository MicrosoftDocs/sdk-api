---
UID: NF:winuser.CreateIconFromResource
title: CreateIconFromResource function
author: windows-sdk-content
description: Creates an icon or cursor from resource bits describing the icon.
old-location: menurc\createiconfromresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconfromresource.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateIconFromResource, CreateIconFromResource function [Menus and Other Resources], _win32_CreateIconFromResource, _win32_createiconfromresource_cpp, menurc.createiconfromresource, winui._win32_createiconfromresource, winuser/CreateIconFromResource
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
api_name:
 - CreateIconFromResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateIconFromResource
: 
---

# CreateIconFromResource function


## -description


Creates an icon or cursor from resource bits describing the icon.

To specify a desired height or width, use the <a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a> function.


## -parameters




### -param presbits [in]

Type: <b>PBYTE</b>

The buffer containing the icon or cursor resource bits. These bits are typically loaded by calls to the <a href="https://msdn.microsoft.com/en-us/library/ms648073(v=VS.85).aspx">LookupIconIdFromDirectory</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648074(v=VS.85).aspx">LookupIconIdFromDirectoryEx</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a> functions. 


### -param dwResSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the set of bits pointed to by the <i>presbits</i> parameter. 


### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is to be created. If this parameter is <b>TRUE</b>, an icon is to be created. If it is <b>FALSE</b>, a cursor is to be created. 


### -param dwVer [in]

Type: <b>DWORD</b>

The version number of the icon or cursor format for the resource bits pointed to by the <i>presbits</i> parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CreateIconFromResource</b>, <a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648062(v=VS.85).aspx">CreateIconIndirect</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648070(v=VS.85).aspx">GetIconInfo</a>, <a href="https://msdn.microsoft.com/en-us/library/ms648073(v=VS.85).aspx">LookupIconIdFromDirectory</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms648074(v=VS.85).aspx">LookupIconIdFromDirectoryEx</a> functions allow shell applications and icon browsers to examine and use resources throughout the system. 

The <b>CreateIconFromResource</b> function calls <a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a> passing <code>LR_DEFAULTSIZE|LR_SHARED</code> as flags.

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648062(v=VS.85).aspx">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648070(v=VS.85).aspx">GetIconInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646973(v=VS.85).aspx">Icons</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648046(v=VS.85).aspx">LoadResource</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648073(v=VS.85).aspx">LookupIconIdFromDirectory</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648074(v=VS.85).aspx">LookupIconIdFromDirectoryEx</a>



<b>Reference</b>
 

 


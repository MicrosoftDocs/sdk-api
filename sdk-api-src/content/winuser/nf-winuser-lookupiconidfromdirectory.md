---
UID: NF:winuser.LookupIconIdFromDirectory
title: LookupIconIdFromDirectory function
author: windows-sdk-content
description: Searches through icon or cursor data for the icon or cursor that best fits the current display device.
old-location: menurc\lookupiconidfromdirectory.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\lookupiconidfromdirectory.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LookupIconIdFromDirectory, LookupIconIdFromDirectory function [Menus and Other Resources], _win32_LookupIconIdFromDirectory, _win32_lookupiconidfromdirectory_cpp, menurc.lookupiconidfromdirectory, winui._win32_lookupiconidfromdirectory, winuser/LookupIconIdFromDirectory
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
 - LookupIconIdFromDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LookupIconIdFromDirectory
: 
---

# LookupIconIdFromDirectory function


## -description


Searches through icon or cursor data for the icon or cursor that best fits the current display device.

To specify a desired height or width, use the <a href="https://msdn.microsoft.com/5ab25565-30a5-4d4f-bf41-2ce3948d6f2f">LookupIconIdFromDirectoryEx</a> function.


## -parameters




### -param presbits [in]

Type: <b>PBYTE</b>

The icon or cursor directory data. Because this function does not validate the resource data, it causes a general protection (GP) fault or returns an undefined value if <i>presbits</i> is not pointing to valid resource data. 


### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is sought. If this parameter is <b>TRUE</b>, the function is searching for an icon; if the parameter is <b>FALSE</b>, the function is searching for a cursor. 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is an integer resource identifier for the icon or cursor that best fits the current display device. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A resource file of type <b>RT_GROUP_ICON</b> (<b>RT_GROUP_CURSOR</b> indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. <b>LookupIconIdFromDirectory</b> searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The <a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a> and <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> functions use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro with this identifier to locate the resource in the module. 

The icon directory is loaded from a resource file with resource type <b>RT_GROUP_ICON</b> (or <b>RT_GROUP_CURSOR</b> for cursors), and an integer resource name for the specific icon to be loaded. <b>LookupIconIdFromDirectory</b> returns an integer identifier that is the resource name of the icon that best fits the current display device. 

The <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>, <a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>, and <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> functions use this function to search the specified resource data for the icon or cursor that best fits the current display device. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c5a1c301-0b1f-49b7-9648-9cf706b74e05">CreateIconFromResource</a>



<a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<a href="https://msdn.microsoft.com/94cc619b-1ca8-4268-9af3-d10d221e093e">GetIconInfo</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<a href="https://msdn.microsoft.com/5ab25565-30a5-4d4f-bf41-2ce3948d6f2f">LookupIconIdFromDirectoryEx</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 


---
UID: NF:winuser.LookupIconIdFromDirectoryEx
title: LookupIconIdFromDirectoryEx function
author: windows-sdk-content
description: Searches through icon or cursor data for the icon or cursor that best fits the current display device.
old-location: menurc\lookupiconidfromdirectoryex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\lookupiconidfromdirectoryex.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LR_DEFAULTCOLOR, LR_MONOCHROME, LookupIconIdFromDirectoryEx, LookupIconIdFromDirectoryEx function [Menus and Other Resources], _win32_LookupIconIdFromDirectoryEx, _win32_lookupiconidfromdirectoryex_cpp, menurc.lookupiconidfromdirectoryex, winui._win32_lookupiconidfromdirectoryex, winuser/LookupIconIdFromDirectoryEx
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
 - LookupIconIdFromDirectoryEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LookupIconIdFromDirectoryEx function


## -description


Searches through icon or cursor data for the icon or cursor that best fits the current display device. 


## -parameters




### -param presbits [in]

Type: <b>PBYTE</b>

The icon or cursor directory data. Because this function does not validate the resource data, it causes a general protection (GP) fault or returns an undefined value if <i>presbits</i> is not pointing to valid resource data. 


### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is sought. If this parameter is <b>TRUE</b>, the function is searching for an icon; if the parameter is <b>FALSE</b>, the function is searching for a cursor. 


### -param cxDesired [in]

Type: <b>int</b>

The desired width, in pixels, of the icon. If this parameter is zero, the function uses the <b>SM_CXICON</b> or <b>SM_CXCURSOR</b> system metric value. 


### -param cyDesired [in]

Type: <b>int</b>

The desired height, in pixels, of the icon. If this parameter is zero, the function uses the <b>SM_CYICON</b> or <b>SM_CYCURSOR</b> system metric value. 


### -param Flags [in]

Type: <b>UINT</b>

A combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTCOLOR"></a><a id="lr_defaultcolor"></a><dl>
<dt><b>LR_DEFAULTCOLOR</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Uses the default color format.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_MONOCHROME"></a><a id="lr_monochrome"></a><dl>
<dt><b>LR_MONOCHROME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Creates a monochrome icon or cursor. 

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is an integer resource identifier for the icon or cursor that best fits the current display device. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A resource file of type <b>RT_GROUP_ICON</b> (<b>RT_GROUP_CURSOR</b> indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. <b>LookupIconIdFromDirectoryEx</b> searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The <a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a> and <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> functions use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro with this identifier to locate the resource in the module. 

The icon directory is loaded from a resource file with resource type <b>RT_GROUP_ICON</b> (or <b>RT_GROUP_CURSOR</b> for cursors), and an integer resource name for the specific icon to be loaded. <b>LookupIconIdFromDirectoryEx</b> returns an integer identifier that is the resource name of the icon that best fits the current display device. 

The <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>, <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>, and <a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a> functions use this function to search the specified resource data for the icon or cursor that best fits the current display device. 


#### Examples

For an example, see <a href="using_icons.htm">Sharing Icon Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a>



<a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<a href="https://msdn.microsoft.com/94cc619b-1ca8-4268-9af3-d10d221e093e">GetIconInfo</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<a href="https://msdn.microsoft.com/4a934e23-597e-48c3-a5f4-9bcf6713dda6">LookupIconIdFromDirectory</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 


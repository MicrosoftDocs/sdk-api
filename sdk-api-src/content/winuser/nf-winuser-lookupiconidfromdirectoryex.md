---
UID: NF:winuser.LookupIconIdFromDirectoryEx
title: LookupIconIdFromDirectoryEx function (winuser.h)
description: Searches through icon or cursor data for the icon or cursor that best fits the current display device.helpviewer_keywords: ["LR_DEFAULTCOLOR","LR_MONOCHROME","LookupIconIdFromDirectoryEx","LookupIconIdFromDirectoryEx function [Menus and Other Resources]","_win32_LookupIconIdFromDirectoryEx","_win32_lookupiconidfromdirectoryex_cpp","menurc.lookupiconidfromdirectoryex","winui._win32_lookupiconidfromdirectoryex","winuser/LookupIconIdFromDirectoryEx"]
old-location: menurc\lookupiconidfromdirectoryex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\lookupiconidfromdirectoryex.htm
ms.date: 12/05/2018
ms.keywords: LR_DEFAULTCOLOR, LR_MONOCHROME, LookupIconIdFromDirectoryEx, LookupIconIdFromDirectoryEx function [Menus and Other Resources], _win32_LookupIconIdFromDirectoryEx, _win32_lookupiconidfromdirectoryex_cpp, menurc.lookupiconidfromdirectoryex, winui._win32_lookupiconidfromdirectoryex, winuser/LookupIconIdFromDirectoryEx
f1_keywords:
- winuser/LookupIconIdFromDirectoryEx
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



A resource file of type <b>RT_GROUP_ICON</b> (<b>RT_GROUP_CURSOR</b> indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. <b>LookupIconIdFromDirectoryEx</b> searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> functions use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro with this identifier to locate the resource in the module. 

The icon directory is loaded from a resource file with resource type <b>RT_GROUP_ICON</b> (or <b>RT_GROUP_CURSOR</b> for cursors), and an integer resource name for the specific icon to be loaded. <b>LookupIconIdFromDirectoryEx</b> returns an integer identifier that is the resource name of the icon that best fits the current display device. 

The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a> functions use this function to search the specified resource data for the icon or cursor that best fits the current display device. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-icons">Sharing Icon Resources</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/icons">Icons</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 


---
UID: NF:winuser.LoadIconA
title: LoadIconA function
author: windows-sdk-content
description: Loads the specified icon resource from the executable (.exe) file associated with an application instance.
old-location: menurc\loadicon.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\loadicon.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDI_APPLICATION, IDI_ASTERISK, IDI_ERROR, IDI_EXCLAMATION, IDI_HAND, IDI_INFORMATION, IDI_QUESTION, IDI_SHIELD, IDI_WARNING, IDI_WINLOGO, LoadIcon, LoadIcon function [Menus and Other Resources], LoadIconA, LoadIconW, _win32_LoadIcon, _win32_loadicon_cpp, menurc.loadicon, winui._win32_loadicon, winuser/LoadIcon, winuser/LoadIconA, winuser/LoadIconW
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
req.unicode-ansi: LoadIconW (Unicode) and LoadIconA (ANSI)
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
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - LoadIcon
 - LoadIconA
 - LoadIconW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadIconA function


## -description


Loads the specified icon resource from the executable (.exe) file associated with an application instance.
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> function.</div><div> </div>

## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the icon to be loaded. This parameter must be <b>NULL</b> when a standard icon is being loaded. 


### -param lpIconName [in]

Type: <b>LPCTSTR</b>

The name of the icon resource to be loaded. Alternatively, this parameter can contain the resource identifier in the low-order word and zero in the high-order word. Use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro to create this value.

To use one of the predefined icons, set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpIconName</i> parameter to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDI_APPLICATION"></a><a id="idi_application"></a><dl>
<dt><b>IDI_APPLICATION</b></dt>
<dt>MAKEINTRESOURCE(32512)</dt>
</dl>
</td>
<td width="60%">
Default application icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ASTERISK"></a><a id="idi_asterisk"></a><dl>
<dt><b>IDI_ASTERISK</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Asterisk icon. Same as <b>IDI_INFORMATION</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ERROR"></a><a id="idi_error"></a><dl>
<dt><b>IDI_ERROR</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
Hand-shaped icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_EXCLAMATION"></a><a id="idi_exclamation"></a><dl>
<dt><b>IDI_EXCLAMATION</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Exclamation point icon. Same as <b>IDI_WARNING</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_HAND"></a><a id="idi_hand"></a><dl>
<dt><b>IDI_HAND</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
Hand-shaped icon. Same as <b>IDI_ERROR</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_INFORMATION"></a><a id="idi_information"></a><dl>
<dt><b>IDI_INFORMATION</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Asterisk icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_QUESTION"></a><a id="idi_question"></a><dl>
<dt><b>IDI_QUESTION</b></dt>
<dt>MAKEINTRESOURCE(32514)</dt>
</dl>
</td>
<td width="60%">
Question mark icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_SHIELD"></a><a id="idi_shield"></a><dl>
<dt><b>IDI_SHIELD</b></dt>
<dt>MAKEINTRESOURCE(32518)</dt>
</dl>
</td>
<td width="60%">
Security Shield icon. 

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WARNING"></a><a id="idi_warning"></a><dl>
<dt><b>IDI_WARNING</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Exclamation point icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WINLOGO"></a><a id="idi_winlogo"></a><dl>
<dt><b>IDI_WINLOGO</b></dt>
<dt>MAKEINTRESOURCE(32517)</dt>
</dl>
</td>
<td width="60%">
 
						Default application icon.

<b>Windows 2000:  </b>Windows logo icon.

</td>
</tr>
</table>
 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the newly loaded icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>LoadIcon</b> loads the icon resource only if it has not been loaded; otherwise, it retrieves a handle to the existing resource. The function searches the icon resource for the icon most appropriate for the current display. The icon resource can be a color or monochrome bitmap. 

<b>LoadIcon</b> can only load an icon whose size conforms to the <b>SM_CXICON</b> and <b>SM_CYICON</b> system metric values. Use the <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> function to load icons of other sizes.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<b>Reference</b>
 

 


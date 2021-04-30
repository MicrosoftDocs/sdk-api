---
UID: NF:commctrl.LoadIconWithScaleDown
title: LoadIconWithScaleDown function (commctrl.h)
description: Loads an icon. If the icon is not a standard size, this function scales down a larger image instead of scaling up a smaller image.
helpviewer_keywords: ["IDI_APPLICATION","IDI_ASTERISK","IDI_ERROR","IDI_EXCLAMATION","IDI_HAND","IDI_INFORMATION","IDI_QUESTION","IDI_SHIELD","IDI_WARNING","IDI_WINLOGO","LoadIconWithScaleDown","LoadIconWithScaleDown function [Windows Controls]","_shell_LoadIconWithScaleDown","_shell_LoadIconWithScaleDown_cpp","commctrl/LoadIconWithScaleDown","controls.LoadIconWithScaleDown","controls._shell_LoadIconWithScaleDown"]
old-location: controls\LoadIconWithScaleDown.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\loadiconwithscaledown.htm
ms.date: 12/05/2018
ms.keywords: IDI_APPLICATION, IDI_ASTERISK, IDI_ERROR, IDI_EXCLAMATION, IDI_HAND, IDI_INFORMATION, IDI_QUESTION, IDI_SHIELD, IDI_WARNING, IDI_WINLOGO, LoadIconWithScaleDown, LoadIconWithScaleDown function [Windows Controls], _shell_LoadIconWithScaleDown, _shell_LoadIconWithScaleDown_cpp, commctrl/LoadIconWithScaleDown, controls.LoadIconWithScaleDown, controls._shell_LoadIconWithScaleDown
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadIconWithScaleDown
 - commctrl/LoadIconWithScaleDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - LoadIconWithScaleDown
---

# LoadIconWithScaleDown function


## -description

Loads an icon. If the icon is not a standard size, this function scales down a larger image instead of scaling up a smaller image.

## -parameters

### -param hinst [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

A handle to the module of either a DLL or executable (.exe) file that contains the icon to be loaded. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandle</a>.

                    

To load a predefined icon or a standalone icon file, set this parameter to <b>NULL</b>.

### -param pszName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

A pointer to a null-terminated, Unicode buffer that contains location information about the icon to load. 


                    

If <i>hinst</i> is non-<b>NULL</b>, <i>pszName</i>  specifies the icon resource either by name or ordinal. This ordinal must be packaged by using the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.

If <i>hinst</i> is <b>NULL</b>, <i>pszName</i> specifies either the name of a standalone icon (.ico) file or the identifier of a predefined icon to load. The following identifiers are recognized. To pass these constants to the <b>LoadIconWithScaleDown</b> function, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. For example, to load the IDI_ERROR icon, pass <code>MAKEINTRESOURCE(IDI_ERROR)</code> as the <i>pszName</i> parameter and <b>NULL</b> as the <i>hinst</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDI_APPLICATION"></a><a id="idi_application"></a><dl>
<dt><b>IDI_APPLICATION</b></dt>
</dl>
</td>
<td width="60%">
Default application icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ASTERISK"></a><a id="idi_asterisk"></a><dl>
<dt><b>IDI_ASTERISK</b></dt>
</dl>
</td>
<td width="60%">
Same as IDI_INFORMATION.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ERROR"></a><a id="idi_error"></a><dl>
<dt><b>IDI_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Hand-shaped icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_EXCLAMATION"></a><a id="idi_exclamation"></a><dl>
<dt><b>IDI_EXCLAMATION</b></dt>
</dl>
</td>
<td width="60%">
Same as IDI_WARNING.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_HAND"></a><a id="idi_hand"></a><dl>
<dt><b>IDI_HAND</b></dt>
</dl>
</td>
<td width="60%">
Same as IDI_ERROR. 

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_INFORMATION"></a><a id="idi_information"></a><dl>
<dt><b>IDI_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Asterisk icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_QUESTION"></a><a id="idi_question"></a><dl>
<dt><b>IDI_QUESTION</b></dt>
</dl>
</td>
<td width="60%">
Question mark icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WARNING"></a><a id="idi_warning"></a><dl>
<dt><b>IDI_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Exclamation point icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WINLOGO"></a><a id="idi_winlogo"></a><dl>
<dt><b>IDI_WINLOGO</b></dt>
</dl>
</td>
<td width="60%">
Windows logo icon. 
						

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_SHIELD"></a><a id="idi_shield"></a><dl>
<dt><b>IDI_SHIELD</b></dt>
</dl>
</td>
<td width="60%">
Security Shield icon.

</td>
</tr>
</table>

### -param cx [in]

Type: <b>int</b>

The desired width, in pixels, of the icon.

### -param cy [in]

Type: <b>int</b>

The desired height, in pixels, of the icon.

### -param phico [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a>*</b>

When this function returns, contains a pointer to the handle of the loaded icon.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The contents of the buffer pointed to by <i>pszName</i> do not fit any of the expected interpretations.

</td>
</tr>
</table>

## -remarks

This function will first search the icon file for an icon having exactly the same size. If a match is not found, then unless both <i>cx</i> and <i>cy</i> match one of the standard icon sizes—16, 32, 48, or 256 pixels— the next largest icon is selected and then scaled down to the desired size. For example, if an icon with an x dimension of 40 pixels is requested by the callign application, the 48-pixel icon is used and scaled down to 40 pixels. In contrast, the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_loadimagea">LoadImage</a> function selects the 32-pixel icon and scales it up to 40 pixels.

If the function is unable to locate a larger icon, it defaults to the standard behavior of finding the next smallest icon and scaling it up to the desired size.
---
UID: NF:wingdi.UpdateICMRegKeyA
title: UpdateICMRegKeyA function (wingdi.h)
description: The UpdateICMRegKey function manages color profiles and Color Management Modules in the system. (ANSI)
helpviewer_keywords: ["ICM_ADDPROFILE", "ICM_DELETEPROFILE", "ICM_QUERYMATCH", "ICM_QUERYPROFILE", "ICM_REGISTERICMATCHER", "ICM_SETDEFAULTPROFILE", "ICM_UNREGISTERICMATCHER", "UpdateICMRegKeyA", "wingdi/UpdateICMRegKeyA"]
old-location: wcs\updateicmregkey.htm
tech.root: WCS
ms.assetid: 705b9671-7bf2-4a47-a3a5-42dd0f334338
ms.date: 12/05/2018
ms.keywords: ICM_ADDPROFILE, ICM_DELETEPROFILE, ICM_QUERYMATCH, ICM_QUERYPROFILE, ICM_REGISTERICMATCHER, ICM_SETDEFAULTPROFILE, ICM_UNREGISTERICMATCHER, UpdateICMRegKey, UpdateICMRegKey function [Windows Color System], UpdateICMRegKeyA, UpdateICMRegKeyW, _color_UpdateICMRegKey, wcs.updateicmregkey, wingdi/UpdateICMRegKey, wingdi/UpdateICMRegKeyA, wingdi/UpdateICMRegKeyW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UpdateICMRegKeyW (Unicode) and UpdateICMRegKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdateICMRegKeyA
 - wingdi/UpdateICMRegKeyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - UpdateICMRegKey
 - UpdateICMRegKeyA
 - UpdateICMRegKeyW
---

# UpdateICMRegKeyA function


## -description

<i>(Obsolete; retained for backward compatibility)</i>

The <b>UpdateICMRegKey</b> function manages color profiles and Color Management Modules in the system.

## -parameters

### -param reserved

Reserved, must be set to zero.

### -param lpszCMID

Points to a string that specifies the ICC profile identifier for the color management DLL to use with the profile.

### -param lpszFileName

Points to a fully qualified ICC color profile file name or to a <b>DEVMODE</b> structure.

### -param command

Specifies a function to execute. It can have one of the following values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICM_ADDPROFILE"></a><a id="icm_addprofile"></a><dl>
<dt><b>ICM_ADDPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Installs the ICC profile in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_DELETEPROFILE"></a><a id="icm_deleteprofile"></a><dl>
<dt><b>ICM_DELETEPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the ICC profile from the system, but does not delete the file.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_QUERYPROFILE"></a><a id="icm_queryprofile"></a><dl>
<dt><b>ICM_QUERYPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the profile is already installed in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_SETDEFAULTPROFILE"></a><a id="icm_setdefaultprofile"></a><dl>
<dt><b>ICM_SETDEFAULTPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Makes the profile first among equals.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_REGISTERICMATCHER"></a><a id="icm_registericmatcher"></a><dl>
<dt><b>ICM_REGISTERICMATCHER</b></dt>
</dl>
</td>
<td width="60%">
Registers a CMM in the system. The <i>pszFileName</i> parameter points to a fully qualified path for the CMM DLL. The <i>lpszCMID</i> parameter points to a <b>DWORD</b> identifying the CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_UNREGISTERICMATCHER"></a><a id="icm_unregistericmatcher"></a><dl>
<dt><b>ICM_UNREGISTERICMATCHER</b></dt>
</dl>
</td>
<td width="60%">
Unregisters the CMM from the system. The <i>lpszCMID</i> parameter points to a <b>DWORD</b> identifying the CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_QUERYMATCH"></a><a id="icm_querymatch"></a><dl>
<dt><b>ICM_QUERYMATCH</b></dt>
</dl>
</td>
<td width="60%">
Determines whether a profile exists based on the <b>DEVMODE</b> structure pointed to by the <i>pszFileName</i> parameter.

</td>
</tr>
</table>

## -returns

If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

## -remarks

Not all parameters are used by all functions. The <i>nCommand</i> parameter specifies the function to execute.

This function is retained for backward compatibility and may be removed in future versions of ICM.

<b>Windows 95/98/Me: </b><b>UpdateICMRegKeyW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines UpdateICMRegKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Obsolete WCS functions](/windows/win32/wcs/obsolete-wcs-functions)

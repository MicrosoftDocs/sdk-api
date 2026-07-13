---
UID: NF:wingdi.GetICMProfileA
title: GetICMProfileA function (wingdi.h)
description: The GetICMProfile function retrieves the file name of the current output color profile for a specified device context. (ANSI)
helpviewer_keywords: ["GetICMProfileA", "wingdi/GetICMProfileA"]
old-location: wcs\geticmprofile.htm
tech.root: WCS
ms.assetid: 1e16771a-80c5-47bb-9c98-14169d4dd773
ms.date: 12/05/2018
ms.keywords: GetICMProfile, GetICMProfile function [Windows Color System], GetICMProfileA, GetICMProfileW, _color_GetICMProfile, wcs.geticmprofile, wingdi/GetICMProfile, wingdi/GetICMProfileA, wingdi/GetICMProfileW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetICMProfileW (Unicode) and GetICMProfileA (ANSI)
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
 - GetICMProfileA
 - wingdi/GetICMProfileA
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
 - GetICMProfile
 - GetICMProfileA
 - GetICMProfileW
---

# GetICMProfileA function


## -description

The <b>GetICMProfile</b> function retrieves the file name of the current output color profile for a specified device context.

## -parameters

### -param hdc

Specifies a device context from which to retrieve the color profile.

### -param pBufSize

Pointer to a <b>DWORD</b> that contains the size of the buffer pointed to by <i>lpszFilename</i>. For the ANSI version of this function, the size is in bytes. For the Unicode version, the size is in WCHARs. If this function is successful, on return this parameter contains the size of the buffer actually used. However, if the buffer is not large enough, this function returns <b>FALSE</b>. In this case, the <b>GetLastError()</b> function returns ERROR_INSUFFICIENT_BUFFER and the <b>DWORD</b> pointed to by this parameter contains the size needed for the <i>lpszFilename</i> buffer.

### -param pszFilename

Points to the buffer that receives the path name of the profile.

## -returns

If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if the <i>lpszFilename</i> parameter is <b>NULL</b> and the size required for the buffer is copied into <i>lpcbName.</i>

If this function fails, the return value is <b>FALSE</b>.

## -remarks

<b>GetICMProfile</b> obtains the file name of the current output profile regardless of whether or not color management is enabled for the device context.

Given a device context, <b>GetICMProfile</b> will output, through the parameter <i>lpszFilename</i>, the path name of the file containing the color profile currently being used by the device context. It will also output, through the parameter <i>lpcbName</i>, the length of the string containing the path name.

It is possible that the profile name returned by <b>GetICMProfile</b> will not be in the list of profiles returned by <a href="/windows/desktop/api/wingdi/nf-wingdi-enumicmprofilesa">EnumICMProfiles</a>. The <b>EnumICMProfiles</b> function returns all color space profiles that are associated with a device context (DC) whose settings match that of the DC. If the <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a> function is used to set the current profile, a profile may be associated with the DC that does not match its settings. For instance, the <b>SetICMProfile</b> function can be used to associate the device-independent sRGB profile with a DC. This profile will be used as the current WCS profile for that DC, and calls to <b>GetICMProfile</b> will return its file name. However, the profile will not appear in the list of profiles that is returned from <b>EnumICMProfiles</b>.

If this function is called before any calls to the <b>SetICMProfile</b> function, it can be used to get the default profile for a device context.

<b>Windows 95/98/Me: </b><b>GetICMProfileW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines GetICMProfile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [DeleteColorSpaceW](/windows/win32/api/wingdi/nf-wingdi-deletecolorspace)
* [ICMENUMPROCA callback function](/windows/win32/api/wingdi/nc-wingdi-icmenumproca)
* [EnumICMProfilesW](/windows/win32/api/wingdi/nf-wingdi-enumicmprofilesw)
* [SetICMProfileW](/windows/win32/api/wingdi/nf-wingdi-seticmprofilew)

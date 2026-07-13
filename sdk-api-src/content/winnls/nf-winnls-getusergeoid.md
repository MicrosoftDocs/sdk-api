---
UID: NF:winnls.GetUserGeoID
title: GetUserGeoID function (winnls.h)
description: Retrieves information about the geographical location of the user. For more information, see Table of Geographical Locations.
helpviewer_keywords: ["GetUserGeoID","GetUserGeoID function [Internationalization for Windows Applications]","_win32_GetUserGeoID","intl.getusergeoid","winnls/GetUserGeoID"]
old-location: intl\getusergeoid.htm
tech.root: Intl
ms.assetid: 9d4d196d-4000-4866-a4c7-e7b9cb669c6f
ms.date: 12/05/2018
ms.keywords: GetUserGeoID, GetUserGeoID function [Internationalization for Windows Applications], _win32_GetUserGeoID, intl.getusergeoid, winnls/GetUserGeoID
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetUserGeoID
 - winnls/GetUserGeoID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUserGeoID
---

# GetUserGeoID function


## -description

<p class="CCE_Message">[<b>GetUserGeoID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultgeoname">GetUserDefaultGeoName</a>.

]

Retrieves information about the geographical location of the user. For more information, see <a href="/windows/desktop/Intl/table-of-geographical-locations">Table of Geographical Locations</a>.

## -parameters

### -param GeoClass [in]

Geographical location class to return. Possible values are defined by the <a href="/windows/desktop/api/winnls/ne-winnls-sysgeoclass">SYSGEOCLASS</a> enumeration.

## -returns

Returns the geographical location identifier of the user if <a href="/windows/desktop/api/winnls/nf-winnls-setusergeoid">SetUserGeoID</a> has been called before to set the identifier.

If no geographical location identifier has been set for the user, the function returns GEOID_NOT_AVAILABLE.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultgeoname">GetUserDefaultGeoName</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/ne-winnls-sysgeoclass">SYSGEOCLASS</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setusergeoid">SetUserGeoID</a>
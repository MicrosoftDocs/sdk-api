---
UID: NF:shlwapi.GetAcceptLanguagesA
title: GetAcceptLanguagesA function (shlwapi.h)
description: Retrieves a string used with websites when specifying language preferences. (ANSI)
helpviewer_keywords: ["GetAcceptLanguagesA", "shlwapi/GetAcceptLanguagesA"]
old-location: shell\GetAcceptLanguages.htm
tech.root: shell
ms.assetid: a680a7fd-f980-485d-b52a-eb4d482ebc17
ms.date: 12/05/2018
ms.keywords: GetAcceptLanguages, GetAcceptLanguages function [Windows Shell], GetAcceptLanguagesA, GetAcceptLanguagesW, _shell_GetAcceptLanguages, shell.GetAcceptLanguages, shlwapi/GetAcceptLanguages, shlwapi/GetAcceptLanguagesA, shlwapi/GetAcceptLanguagesW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAcceptLanguagesW (Unicode) and GetAcceptLanguagesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAcceptLanguagesA
 - shlwapi/GetAcceptLanguagesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - GetAcceptLanguages
 - GetAcceptLanguagesA
 - GetAcceptLanguagesW
---

# GetAcceptLanguagesA function


## -description

Retrieves a string used with websites when specifying language preferences.

## -parameters

### -param pszLanguages [out]

Type: <b>LPTSTR</b>

A pointer to a string that, when this function returns successfully, receives the language preferences information. We recommend that this buffer be of size 2048 characters to ensure sufficient space to return the full string. You can also call this function with this parameter set to NULL to retrieve the size of the string that will be returned.

### -param pcchLanguages [in, out]

Type: <b>DWORD*</b>

A pointer to the size, in characters, of the string at <i>pszLanguages</i>. 
                        
                        

On entry, this value is the size of <i>pszLanguages</i>, including the terminating null character.

On exit, it is the actual size of <i>pszLanguages</i>, not including the terminating null character.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For those versions of Windows that do not include <b>GetAcceptLanguages</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>GetAcceptLanguagesA</b> is ordinal 14 and <b>GetAcceptLanguagesW</b> is ordinal 15.

Some websites offer content in multiple languages. You can specify your language preferences in the Internet Options item in Control Panel. <b>GetAcceptLanguages</b> retrieves a string that represents those preferences. That string is sent in an additional language header when negotiating HTTP connections.

<div class="alert"><b>Note</b>  If your app or service passes language tags from this function to any <a href="/windows/desktop/Intl/national-language-support">National Language Support</a> functions, or to Microsoft .NET, it must first convert the tags through the <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a> function.</div>
<div> </div>



> [!NOTE]
> The shlwapi.h header defines GetAcceptLanguages as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

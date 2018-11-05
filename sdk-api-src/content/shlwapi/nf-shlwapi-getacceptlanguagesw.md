---
UID: NF:shlwapi.GetAcceptLanguagesW
title: GetAcceptLanguagesW function
author: windows-sdk-content
description: Retrieves a string used with websites when specifying language preferences.
old-location: shell\GetAcceptLanguages.htm
tech.root: shell
ms.assetid: a680a7fd-f980-485d-b52a-eb4d482ebc17
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAcceptLanguages, GetAcceptLanguages function [Windows Shell], GetAcceptLanguagesA, GetAcceptLanguagesW, _shell_GetAcceptLanguages, shell.GetAcceptLanguages, shlwapi/GetAcceptLanguages, shlwapi/GetAcceptLanguagesA, shlwapi/GetAcceptLanguagesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAcceptLanguagesW function


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

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For those versions of Windows that do not include <b>GetAcceptLanguages</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>GetAcceptLanguagesA</b> is ordinal 14 and <b>GetAcceptLanguagesW</b> is ordinal 15.

Some websites offer content in multiple languages. You can specify your language preferences in the Internet Options item in Control Panel. <b>GetAcceptLanguages</b> retrieves a string that represents those preferences. That string is sent in an additional language header when negotiating HTTP connections.

<div class="alert"><b>Note</b>  If your app or service passes language tags from this function to any <a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a> functions, or to Microsoft .NET, it must first convert the tags through the <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a> function.</div>
<div> </div>



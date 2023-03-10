---
UID: NF:winineti.CreateMD5SSOHash
title: CreateMD5SSOHash function (winineti.h)
description: The CreateMD5SSOHash function (winineti.h) obtains the default Microsoft Passport password for a specified account or realm, creates an MD5 hash from it, and returns the result.
helpviewer_keywords: ["CreateMD5SSOHash","CreateMD5SSOHash function [WinINet]","wininet.createmd5ssohash","winineti/CreateMD5SSOHash"]
old-location: wininet\createmd5ssohash.htm
tech.root: wininet
ms.assetid: 9aba22d7-a1a9-4b90-bfc6-78df8a8d0ce5
ms.date: 08/15/2022
ms.keywords: CreateMD5SSOHash, CreateMD5SSOHash function [WinINet], wininet.createmd5ssohash, winineti/CreateMD5SSOHash
req.header: winineti.h
req.include-header: Wininet.h
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMD5SSOHash
 - winineti/CreateMD5SSOHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - CreateMD5SSOHash
---

# CreateMD5SSOHash function


## -description

The <b>CreateMD5SSOHash</b> function obtains the default Microsoft Passport password for a specified account or realm, creates an MD5 hash from it using a specified wide-character challenge string, and returns the result as a string of hexadecimal digit bytes.

## -parameters

### -param pszChallengeInfo [in]

Pointer to the wide-character challenge string to use for the MD5 hash.

### -param pwszRealm [in]

Pointer to a string that names a realm for which to obtain the password. This parameter is ignored unless <i>pwszTarget</i> is <b>NULL</b>. If both <i>pwszTarget</i> and <i>pwszRealm</i> are <b>NULL</b>, the default realm is used.

### -param pwszTarget [in]

Pointer to a string that names an account for which to obtain the password. If <i>pwszTarget</i> is <b>NULL</b>, the realm indicated by <i>pwszRealm</i> is used.

### -param pbHexHash [out]

Pointer to an output buffer into which the MD5 hash is returned in hex string format. This buffer must be at least 33 bytes long.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

Once the <b>CreateMD5SSOHash</b> function successfully obtains the Microsoft Passport password for the specified account or realm, it converts both the challenge string and the password from wide characters to multi-byte (generally 8-bit) characters, concatenates them, and uses the RSA library to generate an MD5 hash from the resulting key. It then converts the hash into a <b>null</b>-terminated string of 8-bit hexadecimal digits (using lowercase letters) which it places in the buffer pointed to by the <i>pbHexHash</i> parameter. 

The output buffer pointed to by  <i>pbHexHash</i> must therefore be long enough to accept two bytes for each of the 16 bytes of the hash, plus a terminating <b>null</b> character, for a total of 33 bytes.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/handling-authentication">Handling Authentication</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>

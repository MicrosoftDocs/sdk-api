---
UID: NF:shlwapi.AssocGetPerceivedType
title: AssocGetPerceivedType function (shlwapi.h)
description: Retrieves a file's perceived type based on its extension.
helpviewer_keywords: ["AssocGetPerceivedType","AssocGetPerceivedType function [Windows Shell]","PERCEIVEDFLAG_GDIPLUS","PERCEIVEDFLAG_HARDCODED","PERCEIVEDFLAG_NATIVESUPPORT","PERCEIVEDFLAG_SOFTCODED","PERCEIVEDFLAG_UNDEFINED","PERCEIVEDFLAG_WMSDK","PERCEIVEDFLAG_ZIPFOLDER","_shell_AssocGetPerceivedType","shell.AssocGetPerceivedType","shlwapi/AssocGetPerceivedType"]
old-location: shell\AssocGetPerceivedType.htm
tech.root: shell
ms.assetid: d37f1574-b261-43bf-9712-05a569ab4246
ms.date: 12/05/2018
ms.keywords: AssocGetPerceivedType, AssocGetPerceivedType function [Windows Shell], PERCEIVEDFLAG_GDIPLUS, PERCEIVEDFLAG_HARDCODED, PERCEIVEDFLAG_NATIVESUPPORT, PERCEIVEDFLAG_SOFTCODED, PERCEIVEDFLAG_UNDEFINED, PERCEIVEDFLAG_WMSDK, PERCEIVEDFLAG_ZIPFOLDER, _shell_AssocGetPerceivedType, shell.AssocGetPerceivedType, shlwapi/AssocGetPerceivedType
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AssocGetPerceivedType
 - shlwapi/AssocGetPerceivedType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - ext-ms-win-shell-shlwapi-l1-1-2.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - AssocGetPerceivedType
---

# AssocGetPerceivedType function


## -description

Retrieves a file's perceived type based on its extension.

## -parameters

### -param pszExt [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the file's extension. This should include the leading period, for example ".txt".

### -param ptype [out]

Type: <b><a href="/windows/desktop/api/shtypes/ne-shtypes-perceived">PERCEIVED</a>*</b>

A pointer to a <a href="/windows/desktop/api/shtypes/ne-shtypes-perceived">PERCEIVED</a> value that indicates the perceived type.

### -param pflag [out]

Type: <b>PERCEIVEDFLAG*</b>

A pointer to a value that indicates the source of the perceived type information. One or more of the following values.



#### PERCEIVEDFLAG_UNDEFINED (0x0000)

No perceived type was found (<a href="/windows/desktop/api/shtypes/ne-shtypes-perceived">PERCEIVED_TYPE_UNSPECIFIED</a>).



#### PERCEIVEDFLAG_SOFTCODED (0x0001)

The perceived type was determined through an association in the registry.



#### PERCEIVEDFLAG_HARDCODED (0x0002)

The perceived type is inherently known to Windows.



#### PERCEIVEDFLAG_NATIVESUPPORT (0x0004)

The perceived type was determined through a codec provided with Windows.



#### PERCEIVEDFLAG_GDIPLUS (0x0010)

The perceived type is supported by the GDI+ library.



#### PERCEIVEDFLAG_WMSDK (0x0020)

The perceived type is supported by the Windows Media SDK.



#### PERCEIVEDFLAG_ZIPFOLDER (0x0040)

The perceived type is supported by Windows compressed folders.

### -param ppszType [out, optional]

Type: <b>PWSTR*</b>

If the function returns a success code, this contains the address of a pointer to a buffer that receives the perceived type string, for instance "text" or "video". This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function first compares the extension against a hard-coded set of extensions known to Windows. If that search fails to reveal a match, the registered associations under HKEY_CLASSES_ROOT are searched for a key that matches the extension and contains a PerceivedType value. If that value is found, the extension set is again searched for a match. If again no match is found, the perceived type is determined to be PERCEIVED_TYPE_CUSTOM. If either a key that matches the extension or a PerceivedType value is not found, the perceived type is reported as PERCEIVED_TYPE_UNSPECIFIED.
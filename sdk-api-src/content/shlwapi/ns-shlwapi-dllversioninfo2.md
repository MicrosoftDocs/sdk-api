---
UID: NS:shlwapi._DLLVERSIONINFO2
title: DLLVERSIONINFO2 (shlwapi.h)
description: Receives DLL-specific version information. It is used with the DllGetVersion function.
helpviewer_keywords: ["DLLVERSIONINFO2","DLLVERSIONINFO2 structure [Windows Shell]","_win32_DLLVERSIONINFO2_0rjh","shell.DLLVERSIONINFO2_0rjh","shlwapi/DLLVERSIONINFO2"]
old-location: shell\DLLVERSIONINFO2_0rjh.htm
tech.root: shell
ms.assetid: 1648924d-0727-4cee-80d3-f97550f235cd
ms.date: 12/05/2018
ms.keywords: DLLVERSIONINFO2, DLLVERSIONINFO2 structure [Windows Shell], _win32_DLLVERSIONINFO2_0rjh, shell.DLLVERSIONINFO2_0rjh, shlwapi/DLLVERSIONINFO2
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DLLVERSIONINFO2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DLLVERSIONINFO2
 - shlwapi/_DLLVERSIONINFO2
 - DLLVERSIONINFO2
 - shlwapi/DLLVERSIONINFO2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - DLLVERSIONINFO2
---

# DLLVERSIONINFO2 structure


## -description

Receives DLL-specific version information. It is used with the <a href="/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc">DllGetVersion</a> function.

## -struct-fields

### -field info1

Type: <b><a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo">DLLVERSIONINFO</a></b>

A <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo">DLLVERSIONINFO</a> structure. This member is included to provide backward compatibility with applications that are not expecting a <b>DLLVERSIONINFO2</b> structure.

### -field dwFlags

Type: <b>DWORD</b>

Reserved.

### -field ullVersion

Type: <b>ULONGLONG</b>

A value that contains the version information. It is divided into four 16-bitfields containing the major and minor version numbers, the build number, and the hotfix version, in that order. Use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull">MAKEDLLVERULL</a> macro to construct this value.

## -remarks

Your application must set the <b>cbSize</b> member of the structure pointed to by <b>info1</b> to <b>sizeof(</b><b>DLLVERSIONINFO2</b><b>)</b> before calling <a href="/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc">DllGetVersion</a>. Otherwise, no value will be assigned to the <b>dwFlags</b> or <b>ullVersion</b> member of the <b>DLLVERSIONINFO2</b> structure.
---
UID: NF:shlwapi.MAKEDLLVERULL
title: MAKEDLLVERULL macro (shlwapi.h)
description: Used to pack DLL version information into a ULONGLONG value.
helpviewer_keywords: ["MAKEDLLVERULL","MAKEDLLVERULL macro [Windows Shell]","_win32_MAKEDLLVERULL","shell.MAKEDLLVERULL","shlwapi/MAKEDLLVERULL"]
old-location: shell\MAKEDLLVERULL.htm
tech.root: shell
ms.assetid: 10c75c91-9642-4877-845e-8c6343721b4f
ms.date: 07/01/2025
ms.keywords: MAKEDLLVERULL, MAKEDLLVERULL macro [Windows Shell], _win32_MAKEDLLVERULL, shell.MAKEDLLVERULL, shlwapi/MAKEDLLVERULL
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAKEDLLVERULL
 - shlwapi/MAKEDLLVERULL
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
 - MAKEDLLVERULL
---

# MAKEDLLVERULL macro

## -syntax

```cpp
ULONGLONG MAKEDLLVERULL(
    WORD major,
    WORD minor,
    WORD build,
    WORD qfe
);
```

## -returns

Type: **ULONGLONG**

Returns the version information packed into a ULONGLONG value.


## -description

Used to pack DLL version information into a ULONGLONG value.

## -parameters

### -param major

The major version number.

### -param minor

The minor version number.

### -param build

The build number.

### -param qfe

The hotfix number that identifies the service pack.

## -remarks

This macro is used in conjunction with <a href="/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc">DllGetVersion</a> to pack version information into a form that can easily be compared to the <b>ullVersion</b> member of a <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2">DLLVERSIONINFO2</a> structure. It is defined as follows.

				


```cpp
#define MAKEDLLVERULL(major, minor, build, qfe) \
        (((ULONGLONG)(major) << 48) | \
         ((ULONGLONG)(minor) << 32) | \
         ((ULONGLONG)(build) << 16) | \
         ((ULONGLONG)(   qfe) <<  0))

```


For most purposes, you only need to assign values to the major and minor version numbers. The remaining two parameters can be set to zero. The following code fragment illustrates how to use <b>MAKEDLLVERULL</b> to determine whether a DLL is <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">version 4.71</a> or later. The <b>VersionInfo</b> structure is the <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2">DLLVERSIONINFO2</a> structure returned by <a href="/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc">DllGetVersion</a>.

				


```cpp
if(VersionInfo.ullVersion >= MAKEDLLVERULL(4, 71, 0, 0))
{
    ...
}

```

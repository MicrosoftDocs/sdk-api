---
UID: NF:versionhelpers.IsWindowsVersionOrGreater
title: IsWindowsVersionOrGreater function (versionhelpers.h)
description: Indicates if the current OS version matches, or is greater than, the provided version information.
helpviewer_keywords: ["IsWindowsVersionOrGreater","IsWindowsVersionOrGreater function","base.iswindowsversionorgreater","versionhelpers/IsWindowsVersionOrGreater"]
old-location: base\iswindowsversionorgreater.htm
tech.root: winprog
ms.assetid: B28DFEC0-A94E-49F6-9DF0-4EE470EC4AF5
ms.date: 12/05/2018
ms.keywords: IsWindowsVersionOrGreater, IsWindowsVersionOrGreater function, base.iswindowsversionorgreater, versionhelpers/IsWindowsVersionOrGreater
req.header: versionhelpers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsWindowsVersionOrGreater
 - versionhelpers/IsWindowsVersionOrGreater
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VersionHelpers.h
api_name:
 - IsWindowsVersionOrGreater
---

# IsWindowsVersionOrGreater function


## -description

<div class="alert"><b>Important</b>  You should only use this function if the other provided 
   <a href="/windows/desktop/SysInfo/version-helper-apis">Version Helper functions</a> do not fit within your 
   scenarios.</div><div> </div>Indicates if the current OS version matches, or is greater than, the provided version 
    information. This function is useful in confirming a  version of Windows Server that 
    doesn't share a version number with a client release.

## -parameters

### -param wMajorVersion

The major OS version number.

### -param wMinorVersion

The minor OS version number.

### -param wServicePackMajor

The major Service Pack version number.

## -returns

<b>TRUE</b> if the specified version matches, or is greater than, the version of the 
      current Windows OS; otherwise, <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7orgreater">IsWindows7OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7sp1orgreater">IsWindows7SP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8orgreater">IsWindows8OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8point1orgreater">IsWindows8Point1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistaorgreater">IsWindowsVistaOrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp1orgreater">IsWindowsVistaSP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp2orgreater">IsWindowsVistaSP2OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxporgreater">IsWindowsXPOrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp1orgreater">IsWindowsXPSP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp2orgreater">IsWindowsXPSP2OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a>
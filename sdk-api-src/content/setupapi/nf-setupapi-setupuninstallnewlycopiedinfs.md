---
UID: NF:setupapi.SetupUninstallNewlyCopiedInfs
title: SetupUninstallNewlyCopiedInfs function (setupapi.h)
description: The SetupUninstallNewlyCopiedInfs function uninstalls INF files (.inf), precompiled INF files (.pnf), and catalog files (.cat) that are previously installed during the committal of the specified file queue.
helpviewer_keywords: ["SetupUninstallNewlyCopiedInfs","SetupUninstallNewlyCopiedInfs function [Setup API]","_setupapi_setupuninstallnewlycopiedinfs","setup.setupuninstallnewlycopiedinfs","setupapi/SetupUninstallNewlyCopiedInfs"]
old-location: setup\setupuninstallnewlycopiedinfs.htm
tech.root: setup
ms.assetid: 7bc10d12-0a0e-48b6-9fb4-1bf1c99cc3be
ms.date: 12/05/2018
ms.keywords: SetupUninstallNewlyCopiedInfs, SetupUninstallNewlyCopiedInfs function [Setup API], _setupapi_setupuninstallnewlycopiedinfs, setup.setupuninstallnewlycopiedinfs, setupapi/SetupUninstallNewlyCopiedInfs
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupUninstallNewlyCopiedInfs
 - setupapi/SetupUninstallNewlyCopiedInfs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupUninstallNewlyCopiedInfs
---

# SetupUninstallNewlyCopiedInfs function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupUninstallNewlyCopiedInfs</b> function uninstalls INF files (.inf), precompiled INF files (.pnf), and catalog files (.cat) that are previously installed during the committal of the specified file queue.

A caller of this function must have administrative privileges; otherwise, the function fails.

## -parameters

### -param FileQueue [in]

Handle to an open and committed file queue. This queue contains the newly installed INF, PNF, or CAT files that 
<b>SetupUninstallNewlyCopiedInfs</b> uninstalls.

### -param Flags [in]

Flags to use with 
<b>SetupUninstallNewlyCopiedInfs</b>. No flags are defined currently. This parameter must be 0 (zero).

### -param Reserved [in]

Reserved. This parameter must be <b>NULL</b>.

## -returns

If the parameters passed in are valid, the return value is <b>TRUE</b> (nonzero), which does not necessarily mean that any INFs are uninstalled.

If some of the parameters passed in are invalid, the return value is <b>FALSE</b> (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcommitfilequeuea">SetupCommitFileQueue</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupuninstalloeminfa">SetupUninstallOEMInf</a>
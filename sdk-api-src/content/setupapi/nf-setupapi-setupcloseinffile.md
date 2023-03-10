---
UID: NF:setupapi.SetupCloseInfFile
title: SetupCloseInfFile function (setupapi.h)
description: The SetupCloseInfFile function closes the INF file opened by a call to SetupOpenInfFile. This function closes any INF files appended to it by calling SetupOpenAppendInfFile.
helpviewer_keywords: ["SetupCloseInfFile","SetupCloseInfFile function [Setup API]","_setupapi_setupcloseinffile","setup.setupcloseinffile","setupapi/SetupCloseInfFile"]
old-location: setup\setupcloseinffile.htm
tech.root: setup
ms.assetid: 78b6a69d-e588-45f1-bf5c-a6feaf8b3364
ms.date: 12/05/2018
ms.keywords: SetupCloseInfFile, SetupCloseInfFile function [Setup API], _setupapi_setupcloseinffile, setup.setupcloseinffile, setupapi/SetupCloseInfFile
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
 - SetupCloseInfFile
 - setupapi/SetupCloseInfFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-setupapi-inf-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupCloseInfFile
req.apiset: ext-ms-win-setupapi-inf-l1-1-0 (introduced in Windows 8)
---

# SetupCloseInfFile function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCloseInfFile</b> function closes the INF file opened by a call to 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopeninffilea">SetupOpenInfFile</a>. This function closes any INF files appended to it by 
calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>.

## -parameters

### -param InfHandle [in]

Handle to the INF file to be closed.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopeninffilea">SetupOpenInfFile</a>

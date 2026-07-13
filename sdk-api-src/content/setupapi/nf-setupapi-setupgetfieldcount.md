---
UID: NF:setupapi.SetupGetFieldCount
title: SetupGetFieldCount function (setupapi.h)
description: The SetupGetFieldCount function retrieves the number of fields in the specified line in an INF file.
helpviewer_keywords: ["SetupGetFieldCount","SetupGetFieldCount function [Setup API]","_setupapi_setupgetfieldcount","setup.setupgetfieldcount","setupapi/SetupGetFieldCount"]
old-location: setup\setupgetfieldcount.htm
tech.root: setup
ms.assetid: 7353d52c-7553-4f50-beab-7fcc4db1fe40
ms.date: 12/05/2018
ms.keywords: SetupGetFieldCount, SetupGetFieldCount function [Setup API], _setupapi_setupgetfieldcount, setup.setupgetfieldcount, setupapi/SetupGetFieldCount
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
 - SetupGetFieldCount
 - setupapi/SetupGetFieldCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupGetFieldCount
req.apiset: ext-ms-win-setupapi-inf-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# SetupGetFieldCount function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFieldCount</b> function retrieves the number of fields in the specified line in an INF file.

## -parameters

### -param Context [in]

Pointer to the context for a line in an INF file.

## -returns

This function returns the number of fields on the line. If <i>Context</i> is invalid, 0 is returned. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetlinecounta">SetupGetLineCount</a>

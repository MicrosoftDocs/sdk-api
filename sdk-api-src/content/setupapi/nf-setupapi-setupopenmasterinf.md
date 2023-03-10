---
UID: NF:setupapi.SetupOpenMasterInf
title: SetupOpenMasterInf function (setupapi.h)
description: The SetupOpenMasterInf function opens the master INF file that contains file and layout information for files shipped with Windows.
helpviewer_keywords: ["SetupOpenMasterInf","SetupOpenMasterInf function [Setup API]","_setupapi_setupopenmasterinf","setup.setupopenmasterinf","setupapi/SetupOpenMasterInf"]
old-location: setup\setupopenmasterinf.htm
tech.root: setup
ms.assetid: dbf3fb81-7416-4eb7-95b9-adfc17b2a364
ms.date: 12/05/2018
ms.keywords: SetupOpenMasterInf, SetupOpenMasterInf function [Setup API], _setupapi_setupopenmasterinf, setup.setupopenmasterinf, setupapi/SetupOpenMasterInf
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
 - SetupOpenMasterInf
 - setupapi/SetupOpenMasterInf
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
 - SetupOpenMasterInf
---

# SetupOpenMasterInf function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenMasterInf</b> function opens the master INF file that contains file and layout information for files shipped with Windows.



## -returns

If 
<b>SetupOpenMasterInf</b> is successful, it returns a handle to the opened INF file that contains file/layout information for files shipped with Windows. Otherwise, the return value is INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopeninffilea">SetupOpenInfFile</a>

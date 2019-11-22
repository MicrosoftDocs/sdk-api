---
UID: NF:setupapi.SetupCancelTemporarySourceList
title: SetupCancelTemporarySourceList function (setupapi.h)

description: The SetupCancelTemporarySourceList function cancels any temporary list and no-browse behavior and reestablishes standard list behavior.
old-location: setup\setupcanceltemporarysourcelist.htm
tech.root: SetupApi
ms.assetid: 87ef9425-5dab-442b-a487-3a4789005411

ms.date: 12/05/2018
ms.keywords: SetupCancelTemporarySourceList, SetupCancelTemporarySourceList function [Setup API], _setupapi_setupcanceltemporarysourcelist, setup.setupcanceltemporarysourcelist, setupapi/SetupCancelTemporarySourceList
ms.topic: function
f1_keywords: 
 - "setupapi/SetupCancelTemporarySourceList"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupCancelTemporarySourceList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupCancelTemporarySourceList function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCancelTemporarySourceList</b> function cancels any temporary list and no-browse behavior and reestablishes standard list behavior.


## -parameters






## -returns



If a temporary list was in effect, the return value is a nonzero value. Otherwise, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>
 

 


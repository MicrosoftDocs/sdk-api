---
UID: NF:setupapi.SetupFreeSourceListW
title: SetupFreeSourceListW function (setupapi.h)

description: The SetupFreeSourceList function frees the system resources allocated to a source list.
old-location: setup\setupfreesourcelist.htm
tech.root: SetupApi
ms.assetid: ac326a2c-df67-4a3e-9290-663f84027a48

ms.date: 12/05/2018
ms.keywords: SetupFreeSourceList, SetupFreeSourceList function [Setup API], SetupFreeSourceListA, SetupFreeSourceListW, _setupapi_setupfreesourcelist, setup.setupfreesourcelist, setupapi/SetupFreeSourceList, setupapi/SetupFreeSourceListA, setupapi/SetupFreeSourceListW
ms.topic: function
f1_keywords: 
 - "setupapi/SetupFreeSourceList"
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
req.unicode-ansi: SetupFreeSourceListW (Unicode) and SetupFreeSourceListA (ANSI)
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
 - SetupFreeSourceList
 - SetupFreeSourceListA
 - SetupFreeSourceListW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupFreeSourceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFreeSourceList</b> function frees the system resources allocated to a source list.


## -parameters




### -param List [in, out]

Pointer to an array of sources from 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupquerysourcelista">SetupQuerySourceList</a>. The <b>null</b>-terminated string should not exceed the size of the destination buffer. When the function returns, this pointer is set to <b>NULL</b>.


### -param Count [in]

Number of sources in the list.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupcanceltemporarysourcelist">SetupCancelTemporarySourceList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupsetsourcelista">SetupSetSourceList</a>
 

 


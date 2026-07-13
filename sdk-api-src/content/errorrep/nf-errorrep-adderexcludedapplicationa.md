---
UID: NF:errorrep.AddERExcludedApplicationA
title: AddERExcludedApplicationA function (errorrep.h)
description: Excludes the specified application from error reporting. (ANSI)
helpviewer_keywords: ["AddERExcludedApplicationA", "errorrep/AddERExcludedApplicationA"]
old-location: wer\adderexcludedapplication.htm
tech.root: wer
ms.assetid: 9055437b-2ee2-4f0a-bcef-2b04ac5368b3
ms.date: 12/05/2018
ms.keywords: AddERExcludedApplication, AddERExcludedApplication function [Windows Error Reporting], AddERExcludedApplicationA, AddERExcludedApplicationW, _win32_adderexcludedapplication, base.adderexcludedapplication, errorrep/AddERExcludedApplication, errorrep/AddERExcludedApplicationA, errorrep/AddERExcludedApplicationW, wer.adderexcludedapplication
req.header: errorrep.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddERExcludedApplicationW (Unicode) and AddERExcludedApplicationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Faultrep.lib
req.dll: Faultrep.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddERExcludedApplicationA
 - errorrep/AddERExcludedApplicationA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Faultrep.dll
api_name:
 - AddERExcludedApplication
 - AddERExcludedApplicationA
 - AddERExcludedApplicationW
---

# AddERExcludedApplicationA function


## -description

<p class="CCE_Message">[The AddERExcludedApplication function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/werapi/nf-werapi-weraddexcludedapplication">WerAddExcludedApplication</a> function.]

Excludes the specified application from error reporting.

## -parameters

### -param szApplication [in]

The name of the executable file for the application, including the file name extension. The name cannot contain path information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, see 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function stores the excluded application list under the <b>HKEY_LOCAL_MACHINE</b> hive. The calling process must have permissions to write to this registry hive.





> [!NOTE]
> The errorrep.h header defines AddERExcludedApplication as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/errorrep/nf-errorrep-reportfault">ReportFault</a>



<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>

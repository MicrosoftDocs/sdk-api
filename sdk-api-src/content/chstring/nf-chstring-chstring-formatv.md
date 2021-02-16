---
UID: NF:chstring.CHString.FormatV
title: CHString::FormatV (chstring.h)
description: The FormatV method writes a formatted string and a variable list of arguments to a CHString string.
helpviewer_keywords: ["?FormatV@CHString@@QAEXPBGPAD@Z","?FormatV@CHString@@QEAAXPEBGPEAD@Z","CHString interface [Windows Management Instrumentation]","FormatV method","CHString.FormatV","CHString::FormatV","FormatV","FormatV method [Windows Management Instrumentation]","FormatV method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_formatv","chstring/CHString::FormatV","wmi.chstring_formatv"]
old-location: wmi\chstring_formatv.htm
tech.root: wmi
ms.assetid: 55488cf0-0098-4d5b-b451-a5d56f30ed65
ms.date: 12/05/2018
ms.keywords: ?FormatV@CHString@@QAEXPBGPAD@Z, ?FormatV@CHString@@QEAAXPEBGPEAD@Z, CHString interface [Windows Management Instrumentation],FormatV method, CHString.FormatV, CHString::FormatV, FormatV, FormatV method [Windows Management Instrumentation], FormatV method [Windows Management Instrumentation],CHString interface, _hmm_chstring_formatv, chstring/CHString::FormatV, wmi.chstring_formatv
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::FormatV
 - chstring/CHString::FormatV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.FormatV
 - ?FormatV@CHString@@QAEXPBGPAD@Z
 - ?FormatV@CHString@@QEAAXPEBGPEAD@Z
---

# CHString::FormatV


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>FormatV</b> method writes a formatted string and a variable list of arguments to a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string.

## -parameters

### -param lpszFormat

Format control string.

### -param argList

List of arguments that are passed.

## -remarks

The <b>FormatV</b> method formats and stores a series of characters and values in the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string. The string and arguments are converted and output according to the corresponding format specification in <i>lpszFormat</i>.

If the string object is offered as a parameter to <b>FormatV</b>, the call fails.

<div class="alert"><b>Note</b>  To reduce exposure to security attacks, always use a format string for <b>FormatV</b>. Never use a user-supplied string for the format string. If your format string is stored for a purpose such as localization, ensure that the string is protected from unauthorized write access. If your function writes to a string rather than standard output, you may need to avoid using a trailing "%s" in the format string. For more information, see <a href="https://www.microsoft.com/?ref=go">www.securityfocus.com/archive/1/81565</a> and <a href="https://www.microsoft.com/?ref=go">www.securityfocus.com/archive/1/66842</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-format(uint_---)">CHString::Format</a>
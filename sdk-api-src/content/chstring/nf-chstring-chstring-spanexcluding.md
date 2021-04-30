---
UID: NF:chstring.CHString.SpanExcluding
title: CHString::SpanExcluding (chstring.h)
description: The SpanExcluding method extracts and returns all characters preceding the first occurrence of a character from lpszCharSet.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","SpanExcluding method","CHString.SpanExcluding","CHString::SpanExcluding","SpanExcluding","SpanExcluding method [Windows Management Instrumentation]","SpanExcluding method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_spanexcluding","chstring/CHString::SpanExcluding","wmi.chstring_spanexcluding"]
old-location: wmi\chstring_spanexcluding.htm
tech.root: wmi
ms.assetid: 5ddadf16-0177-4f96-a5ca-e1b8891473e6
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],SpanExcluding method, CHString.SpanExcluding, CHString::SpanExcluding, SpanExcluding, SpanExcluding method [Windows Management Instrumentation], SpanExcluding method [Windows Management Instrumentation],CHString interface, _hmm_chstring_spanexcluding, chstring/CHString::SpanExcluding, wmi.chstring_spanexcluding
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
 - CHString::SpanExcluding
 - chstring/CHString::SpanExcluding
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.SpanExcluding
---

# CHString::SpanExcluding


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SpanExcluding</b> method extracts and returns all characters preceding the first occurrence of a character from <i>lpszCharSet</i>.

## -parameters

### -param lpszCharSet

A string interpreted as a set of characters.

## -returns

The <b>SpanExcluding</b> method returns a substring that begins with the first character in the string and ends with the first character found in the string that is also in <i>lpszCharSet</i>.

If no character in <i>lpszCharSet</i> is found in the string, the method returns the entire string.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-spanincluding">CHString::SpanIncluding</a>
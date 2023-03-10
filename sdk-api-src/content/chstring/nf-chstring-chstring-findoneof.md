---
UID: NF:chstring.CHString.FindOneOf
title: CHString::FindOneOf (chstring.h)
description: The FindOneOf method searches a string for the first character that matches any character contained in lpszCharSet.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","FindOneOf method","CHString.FindOneOf","CHString::FindOneOf","FindOneOf","FindOneOf method [Windows Management Instrumentation]","FindOneOf method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_findoneof","chstring/CHString::FindOneOf","wmi.chstring_findoneof"]
old-location: wmi\chstring_findoneof.htm
tech.root: wmi
ms.assetid: f3f9111d-9191-4ba5-877a-736e11d0a168
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],FindOneOf method, CHString.FindOneOf, CHString::FindOneOf, FindOneOf, FindOneOf method [Windows Management Instrumentation], FindOneOf method [Windows Management Instrumentation],CHString interface, _hmm_chstring_findoneof, chstring/CHString::FindOneOf, wmi.chstring_findoneof
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
 - CHString::FindOneOf
 - chstring/CHString::FindOneOf
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
 - CHString.FindOneOf
---

# CHString::FindOneOf


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>FindOneOf</b> method searches a string for the first character that matches any character contained in <i>lpszCharSet</i>.

## -parameters

### -param lpszCharSet

String that contains characters used in the matching operation.

## -returns

If the method is successful, it returns the zero-based index of the first character in the string that is also in <i>lpszCharSet</i>. If there is no match, the method returns a value of -1.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">CHString::Find</a>
---
UID: NF:chstring.CHString.ReverseFind
title: CHString::ReverseFind (chstring.h)
description: The ReverseFind method searches a CHString string for the last match of a substring. This method is similar to the runtime function, wcsrchr.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","ReverseFind method","CHString.ReverseFind","CHString::ReverseFind","ReverseFind","ReverseFind method [Windows Management Instrumentation]","ReverseFind method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_reversefind","chstring/CHString::ReverseFind","wmi.chstring_reversefind"]
old-location: wmi\chstring_reversefind.htm
tech.root: wmi
ms.assetid: 941c9eb3-a5b8-42b7-bb9f-732eaf1faa24
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],ReverseFind method, CHString.ReverseFind, CHString::ReverseFind, ReverseFind, ReverseFind method [Windows Management Instrumentation], ReverseFind method [Windows Management Instrumentation],CHString interface, _hmm_chstring_reversefind, chstring/CHString::ReverseFind, wmi.chstring_reversefind
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
 - CHString::ReverseFind
 - chstring/CHString::ReverseFind
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
 - CHString.ReverseFind
---

# CHString::ReverseFind


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ReverseFind</b> method searches a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string for the last match of a substring. This method is similar to the runtime function, wcsrchr.

## -parameters

### -param ch

The character that the method searches for.

## -returns

Returns the zero-based index of the last character in the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string that matches the requested character. If the character is not found, the method returns a value of -1.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">CHString::Find</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-findoneof">CHString::FindOneOf</a>
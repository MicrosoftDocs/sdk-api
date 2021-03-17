---
UID: NF:chstring.CHString.Right
title: CHString::Right (chstring.h)
description: Extracts the last nCount characters from a CHString string and returns a copy of the extracted substring.
helpviewer_keywords: ["?Right@CHString@@QBE?AV1@H@Z","?Right@CHString@@QEBA?AV1@H@Z","CHString interface [Windows Management Instrumentation]","Right method","CHString.Right","CHString::Right","Right","Right method [Windows Management Instrumentation]","Right method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_right","chstring/CHString::Right","wmi.chstring_right"]
old-location: wmi\chstring_right.htm
tech.root: wmi
ms.assetid: eccf928f-75ac-4442-90f9-0e0578c5798f
ms.date: 12/05/2018
ms.keywords: ?Right@CHString@@QBE?AV1@H@Z, ?Right@CHString@@QEBA?AV1@H@Z, CHString interface [Windows Management Instrumentation],Right method, CHString.Right, CHString::Right, Right, Right method [Windows Management Instrumentation], Right method [Windows Management Instrumentation],CHString interface, _hmm_chstring_right, chstring/CHString::Right, wmi.chstring_right
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
 - CHString::Right
 - chstring/CHString::Right
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
 - CHString.Right
 - ?Right@CHString@@QBE?AV1@H@Z
 - ?Right@CHString@@QEBA?AV1@H@Z
---

# CHString::Right


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Right</b> method extracts the last (that is, rightmost) <i>nCount</i> characters from a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string and returns a copy of the extracted substring. If <i>nCount</i> exceeds the string length, then the entire string is extracted.

## -parameters

### -param nCount

The number of characters extracted from the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string.

## -returns

Returns a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object that contains a copy of the specified range of characters.

<div class="alert"><b>Note</b>  The returned <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object can be empty.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-left">CHString::Left</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-mid(int_int)">CHString::Mid</a>
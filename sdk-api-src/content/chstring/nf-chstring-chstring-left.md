---
UID: NF:chstring.CHString.Left
title: CHString::Left (chstring.h)
description: Extracts the first nCount characters from a CHString string and returns a copy of the extracted substring.helpviewer_keywords: ["?Left@CHString@@QBE?AV1@H@Z","?Left@CHString@@QEBA?AV1@H@Z","CHString interface [Windows Management Instrumentation]","Left method","CHString.Left","CHString::Left","Left","Left method [Windows Management Instrumentation]","Left method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_left","chstring/CHString::Left","wmi.chstring_left"]
old-location: wmi\chstring_left.htm
tech.root: WmiSdk
ms.assetid: 52219bbb-0a88-47b3-ac6c-ba54d15e8157
ms.date: 12/05/2018
ms.keywords: ?Left@CHString@@QBE?AV1@H@Z, ?Left@CHString@@QEBA?AV1@H@Z, CHString interface [Windows Management Instrumentation],Left method, CHString.Left, CHString::Left, Left, Left method [Windows Management Instrumentation], Left method [Windows Management Instrumentation],CHString interface, _hmm_chstring_left, chstring/CHString::Left, wmi.chstring_left
f1_keywords:
- chstring/CHString.Left
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CHString.Left
- ?Left@CHString@@QBE?AV1@H@Z
- ?Left@CHString@@QEBA?AV1@H@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString::Left


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Left</b> method extracts the first (that is, leftmost) <i>nCount</i> characters from a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string and returns a copy of the extracted substring. If <i>nCount</i> exceeds the string length, then the entire string is extracted.


## -parameters




### -param nCount

The number of characters extracted from the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string.


## -returns



Returns a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string containing a copy of the specified range of characters.

<div class="alert"><b>Note</b>  The returned <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string may be empty.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-mid(int_int)">CHString::Mid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-right">CHString::Right</a>
 

 


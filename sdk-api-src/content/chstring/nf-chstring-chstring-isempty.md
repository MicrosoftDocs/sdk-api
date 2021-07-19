---
UID: NF:chstring.CHString.IsEmpty
title: CHString::IsEmpty (chstring.h)
description: The IsEmpty method tests a CHString string for the empty condition.
helpviewer_keywords: ["?IsEmpty@CHString@@QBEHXZ","?IsEmpty@CHString@@QEBAHXZ","CHString interface [Windows Management Instrumentation]","IsEmpty method","CHString.IsEmpty","CHString::IsEmpty","IsEmpty","IsEmpty method [Windows Management Instrumentation]","IsEmpty method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_isempty","chstring/CHString::IsEmpty","wmi.chstring_isempty"]
old-location: wmi\chstring_isempty.htm
tech.root: wmi
ms.assetid: 06af1063-1e5a-4a09-a0d7-b5567b9efcff
ms.date: 12/05/2018
ms.keywords: ?IsEmpty@CHString@@QBEHXZ, ?IsEmpty@CHString@@QEBAHXZ, CHString interface [Windows Management Instrumentation],IsEmpty method, CHString.IsEmpty, CHString::IsEmpty, IsEmpty, IsEmpty method [Windows Management Instrumentation], IsEmpty method [Windows Management Instrumentation],CHString interface, _hmm_chstring_isempty, chstring/CHString::IsEmpty, wmi.chstring_isempty
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
 - CHString::IsEmpty
 - chstring/CHString::IsEmpty
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
 - CHString.IsEmpty
 - ?IsEmpty@CHString@@QBEHXZ
 - ?IsEmpty@CHString@@QEBAHXZ
---

# CHString::IsEmpty


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>IsEmpty</b> method tests a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string for the empty condition.



## -returns

If the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string has a length of zero, the <b>IsEmpty</b> method returns a nonzero value. If the <b>CHString</b> string has a nonzero length, the method returns zero.

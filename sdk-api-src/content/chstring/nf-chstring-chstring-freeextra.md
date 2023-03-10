---
UID: NF:chstring.CHString.FreeExtra
title: CHString::FreeExtra (chstring.h)
description: The FreeExtra method frees any extra memory that was previously allocated by the string but is no longer needed.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","FreeExtra method","CHString.FreeExtra","CHString::FreeExtra","FreeExtra","FreeExtra method [Windows Management Instrumentation]","FreeExtra method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_freeextra","chstring/CHString::FreeExtra","wmi.chstring_freeextra"]
old-location: wmi\chstring_freeextra.htm
tech.root: wmi
ms.assetid: 4330564e-aeae-4ff3-b01d-eceace721c14
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],FreeExtra method, CHString.FreeExtra, CHString::FreeExtra, FreeExtra, FreeExtra method [Windows Management Instrumentation], FreeExtra method [Windows Management Instrumentation],CHString interface, _hmm_chstring_freeextra, chstring/CHString::FreeExtra, wmi.chstring_freeextra
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
 - CHString::FreeExtra
 - chstring/CHString::FreeExtra
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
 - CHString.FreeExtra
---

# CHString::FreeExtra


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>FreeExtra</b> method frees any extra memory that was previously allocated by the string but is no longer needed. This method, which reallocates the buffer to the exact length returned by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getlength">GetLength</a>, should reduce the memory overhead consumed by the string object.



## -returns

This method does not return a value.

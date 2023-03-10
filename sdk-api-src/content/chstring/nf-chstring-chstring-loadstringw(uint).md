---
UID: NF:chstring.CHString.LoadStringW(UINT)
title: CHString::LoadStringW(UINT) (chstring.h)
description: The LoadStringW method reads a Windows string resource (identified by nID) into an existing CHString object. (overload 1/2)
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","LoadStringW method","CHString.LoadStringW","CHString.LoadStringW(UINT)","CHString::LoadStringW","CHString::LoadStringW(UINT)","LoadStringW","LoadStringW method [Windows Management Instrumentation]","LoadStringW method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_loadstringw","chstring/CHString::LoadStringW","wmi.chstring_loadstringw"]
old-location: wmi\chstring_loadstringw.htm
tech.root: wmi
ms.assetid: b5dca7ce-41b2-4290-bb15-23e0a8d64bd1
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],LoadStringW method, CHString.LoadStringW, CHString.LoadStringW(UINT), CHString::LoadStringW, CHString::LoadStringW(UINT), LoadStringW, LoadStringW method [Windows Management Instrumentation], LoadStringW method [Windows Management Instrumentation],CHString interface, _hmm_chstring_loadstringw, chstring/CHString::LoadStringW, wmi.chstring_loadstringw
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
 - CHString::LoadStringW
 - chstring/CHString::LoadStringW
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
 - CHString.LoadStringW
---

# CHString::LoadStringW(UINT)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>LoadStringW</b> method reads a Windows string resource (identified by <i>nID</i>) into an existing <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object.

## -parameters

### -param nID

Windows string resource identifier.

## -returns

If the <b>LoadStringW</b> method is successful, the resource string is loaded into the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> object, and the method returns a nonzero value. If the method is unsuccessful, it returns zero.

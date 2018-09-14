---
UID: NF:chstring.CHString.LoadStringW(UINT,LPWSTR,UINT)
title: CHString::LoadStringW(UINT,LPWSTR,UINT)
author: windows-sdk-content
description: The LoadStringW method reads a Windows string resource (identified by nID) into an existing CHString object.
old-location: wmi\chstring_loadstringw.htm
tech.root: WmiSdk
ms.assetid: b5dca7ce-41b2-4290-bb15-23e0a8d64bd1
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CHString interface [Windows Management Instrumentation],LoadStringW method, CHString.LoadStringW, CHString.LoadStringW(UINT,LPWSTR,UINT), CHString::LoadStringW, CHString::LoadStringW(UINT,LPWSTR,UINT), LoadStringW, LoadStringW method [Windows Management Instrumentation], LoadStringW method [Windows Management Instrumentation],CHString interface, _hmm_chstring_loadstringw, chstring/CHString::LoadStringW, wmi.chstring_loadstringw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.LoadStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::LoadStringW(UINT,LPWSTR,UINT)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>LoadStringW</b> method reads a Windows string resource (identified by <i>nID</i>) into an existing <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object.


## -parameters




### -param nID

Windows string resource identifier.


### -param lpszBuf

TBD


### -param nMaxBuf

TBD




## -returns



If the <b>LoadStringW</b> method is successful, the resource string is loaded into the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object, and the method returns a nonzero value. If the method is unsuccessful, it returns zero.




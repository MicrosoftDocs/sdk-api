---
UID: NF:chstring.CHString.ReleaseBuffer
title: CHString::ReleaseBuffer (chstring.h)
description: Ends the use of a buffer allocated by GetBuffer.
helpviewer_keywords: ["?ReleaseBuffer@CHString@@QAEXH@Z","?ReleaseBuffer@CHString@@QEAAXH@Z","CHString interface [Windows Management Instrumentation]","ReleaseBuffer method","CHString.ReleaseBuffer","CHString::ReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [Windows Management Instrumentation]","ReleaseBuffer method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_releasebuffer","chstring/CHString::ReleaseBuffer","wmi.chstring_releasebuffer"]
old-location: wmi\chstring_releasebuffer.htm
tech.root: wmi
ms.assetid: 55de2960-8a71-48cc-862b-7cf9a4edf8ea
ms.date: 12/05/2018
ms.keywords: ?ReleaseBuffer@CHString@@QAEXH@Z, ?ReleaseBuffer@CHString@@QEAAXH@Z, CHString interface [Windows Management Instrumentation],ReleaseBuffer method, CHString.ReleaseBuffer, CHString::ReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Windows Management Instrumentation], ReleaseBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_releasebuffer, chstring/CHString::ReleaseBuffer, wmi.chstring_releasebuffer
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
 - CHString::ReleaseBuffer
 - chstring/CHString::ReleaseBuffer
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
 - CHString.ReleaseBuffer
 - ?ReleaseBuffer@CHString@@QAEXH@Z
 - ?ReleaseBuffer@CHString@@QEAAXH@Z
---

# CHString::ReleaseBuffer


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ReleaseBuffer</b> method ends the use of a buffer allocated by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">GetBuffer</a>.

## -parameters

### -param nNewLength

The new length of the string in characters, not counting a terminating <b>null</b> character.

If the string is <b>NULL</b>-terminated, the –1 default value sets the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string size to the current length of the string.

## -returns

This method does not return a value.

## -remarks

If you know that the string in the buffer is <b>NULL</b>-terminated, you can omit the <i>nNewLength</i> parameter. If your string is not <b>NULL</b>-terminated, then use <i>nNewLength</i> to specify its length. The address returned by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">GetBuffer</a> is not valid after the call to <b>ReleaseBuffer</b> or any other <a href="/windows/desktop/WmiSdk/chstring">CHString</a> operation.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">CHString::GetBuffer</a>
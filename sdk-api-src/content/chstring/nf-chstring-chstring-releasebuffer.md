---
UID: NF:chstring.CHString.ReleaseBuffer
title: CHString::ReleaseBuffer
author: windows-sdk-content
description: Ends the use of a buffer allocated by GetBuffer.
old-location: wmi\chstring_releasebuffer.htm
tech.root: WmiSdk
ms.assetid: 55de2960-8a71-48cc-862b-7cf9a4edf8ea
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "?ReleaseBuffer@CHString@@QAEXH@Z, ?ReleaseBuffer@CHString@@QEAAXH@Z, CHString interface [Windows Management Instrumentation],ReleaseBuffer method, CHString.ReleaseBuffer, CHString::ReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Windows Management Instrumentation], ReleaseBuffer method [Windows Management Instrumentation],CHString interface, _hmm_chstring_releasebuffer, chstring/CHString::ReleaseBuffer, wmi.chstring_releasebuffer"
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
 - CHString.ReleaseBuffer
 - ?ReleaseBuffer@CHString@@QAEXH@Z
 - ?ReleaseBuffer@CHString@@QEAAXH@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- chstring.h
: 
- CHString.ReleaseBuffer
: 
---

# CHString::ReleaseBuffer


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ReleaseBuffer</b> method ends the use of a buffer allocated by <a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">GetBuffer</a>.


## -parameters




### -param nNewLength

The new length of the string in characters, not counting a terminating <b>null</b> character.

If the string is <b>NULL</b>-terminated, the –1 default value sets the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string size to the current length of the string.


## -returns



This method does not return a value.




## -remarks



If you know that the string in the buffer is <b>NULL</b>-terminated, you can omit the <i>nNewLength</i> parameter. If your string is not <b>NULL</b>-terminated, then use <i>nNewLength</i> to specify its length. The address returned by <a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">GetBuffer</a> is not valid after the call to <b>ReleaseBuffer</b> or any other <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> operation.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">CHString::GetBuffer</a>
 

 


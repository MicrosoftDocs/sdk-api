---
UID: NF:chstring.CHString.GetLength
title: CHString::GetLength
author: windows-sdk-content
description: The GetLength method gets a count of the number of wide characters in this CHString string. The count does not include a NULL terminator.
old-location: wmi\chstring_getlength.htm
old-project: WmiSdk
ms.assetid: b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "?GetLength@CHString@@QBEHXZ, ?GetLength@CHString@@QEBAHXZ, CHString interface [Windows Management Instrumentation],GetLength method, CHString.GetLength, CHString::GetLength, GetLength, GetLength method [Windows Management Instrumentation], GetLength method [Windows Management Instrumentation],CHString interface, _hmm_chstring_getlength, chstring/CHString::GetLength, wmi.chstring_getlength"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.GetLength
 - ?GetLength@CHString@@QBEHXZ
 - ?GetLength@CHString@@QEBAHXZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::GetLength


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetLength</b> method gets a count of the number of wide characters in this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string. The count does not include a <b>NULL</b> terminator.


## -parameters






## -returns



Returns a count of the number of wide characters in the string, not the number of bytes.




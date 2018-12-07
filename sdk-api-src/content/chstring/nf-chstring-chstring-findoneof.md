---
UID: NF:chstring.CHString.FindOneOf
title: CHString::FindOneOf
author: windows-sdk-content
description: The FindOneOf method searches a string for the first character that matches any character contained in lpszCharSet.
old-location: wmi\chstring_findoneof.htm
tech.root: WmiSdk
ms.assetid: f3f9111d-9191-4ba5-877a-736e11d0a168
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CHString interface [Windows Management Instrumentation],FindOneOf method, CHString.FindOneOf, CHString::FindOneOf, FindOneOf, FindOneOf method [Windows Management Instrumentation], FindOneOf method [Windows Management Instrumentation],CHString interface, _hmm_chstring_findoneof, chstring/CHString::FindOneOf, wmi.chstring_findoneof
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
 - CHString.FindOneOf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::FindOneOf


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>FindOneOf</b> method searches a string for the first character that matches any character contained in <i>lpszCharSet</i>.


## -parameters




### -param lpszCharSet

String that contains characters used in the matching operation.


## -returns



If the method is successful, it returns the zero-based index of the first character in the string that is also in <i>lpszCharSet</i>. If there is no match, the method returns a value of -1.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">CHString::Find</a>
 

 


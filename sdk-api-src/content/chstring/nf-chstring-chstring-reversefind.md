---
UID: NF:chstring.CHString.ReverseFind
title: CHString::ReverseFind method
author: windows-driver-content
description: The ReverseFind method searches a CHString string for the last match of a substring. This method is similar to the runtime function, wcsrchr.
old-location: wmi\chstring_reversefind.htm
old-project: WmiSdk
ms.assetid: 941c9eb3-a5b8-42b7-bb9f-732eaf1faa24
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CHString, CHString interface [Windows Management Instrumentation], ReverseFind method, CHString::ReverseFind, ReverseFind method [Windows Management Instrumentation], ReverseFind method [Windows Management Instrumentation], CHString interface, ReverseFind,CHString.ReverseFind, _hmm_chstring_reversefind, chstring/CHString::ReverseFind, wmi.chstring_reversefind
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
req.typenames: CF_SYNC_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.ReverseFind
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::ReverseFind method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ReverseFind</b> method searches a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string for the last match of a substring. This method is similar to the runtime function, wcsrchr.


## -parameters




### -param ch

The character that the method searches for.


## -returns



Returns the zero-based index of the last character in the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string that matches the requested character. If the character is not found, the method returns a value of -1.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">CHString::Find</a>



<a href="https://msdn.microsoft.com/f3f9111d-9191-4ba5-877a-736e11d0a168">CHString::FindOneOf</a>
 

 


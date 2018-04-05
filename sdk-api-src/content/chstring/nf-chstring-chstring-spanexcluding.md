---
UID: NF:chstring.CHString.SpanExcluding
title: CHString::SpanExcluding method
author: windows-driver-content
description: The SpanExcluding method extracts and returns all characters preceding the first occurrence of a character from lpszCharSet.
old-location: wmi\chstring_spanexcluding.htm
old-project: WmiSdk
ms.assetid: 5ddadf16-0177-4f96-a5ca-e1b8891473e6
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CHString, CHString interface [Windows Management Instrumentation], SpanExcluding method, CHString::SpanExcluding, SpanExcluding method [Windows Management Instrumentation], SpanExcluding method [Windows Management Instrumentation], CHString interface, SpanExcluding,CHString.SpanExcluding, _hmm_chstring_spanexcluding, chstring/CHString::SpanExcluding, wmi.chstring_spanexcluding
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
req.typenames: CF_SYNC_ROOT_STANDARD_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.SpanExcluding
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::SpanExcluding method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SpanExcluding</b> method extracts and returns all characters preceding the first occurrence of a character from <i>lpszCharSet</i>.


## -parameters




### -param lpszCharSet

A string interpreted as a set of characters.


## -returns



The <b>SpanExcluding</b> method returns a substring that begins with the first character in the string and ends with the first character found in the string that is also in <i>lpszCharSet</i>.

If no character in <i>lpszCharSet</i> is found in the string, the method returns the entire string.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/d99ce931-c6ec-4f1c-b4ab-144dc930f990">CHString::SpanIncluding</a>
 

 


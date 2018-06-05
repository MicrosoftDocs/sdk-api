---
UID: NF:chstring.CHString.SetAt
title: CHString::SetAt
author: windows-sdk-content
description: Overwrites one character specified by an index number.
old-location: wmi\chstring_setat.htm
old-project: WmiSdk
ms.assetid: ccac0f07-a272-41b0-950c-7e5d97d9f1d7
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHString interface [Windows Management Instrumentation],SetAt method, CHString.SetAt, CHString::SetAt, SetAt, SetAt method [Windows Management Instrumentation], SetAt method [Windows Management Instrumentation],CHString interface, _hmm_chstring_setat, chstring/CHString::SetAt, wmi.chstring_setat
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.SetAt
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::SetAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetAt</b> method overwrites one character specified by an index number. If the index exceeds the bounds of the existing string,  <b>SetAt</b> does not enlarge the string.


## -parameters




### -param nIndex

Zero-based index of the character in the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0), and less than the value returned by <a href="https://msdn.microsoft.com/b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f">GetLength</a>. The debug version of the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

### -param ch

The character to insert.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/ed038b41-211c-4483-99cd-0bc43b241761">CHString::GetAt</a>
 

 


---
UID: NF:chstring.CHString.Mid
title: CHString::Mid
author: windows-sdk-content
description: The Mid method extracts a substring of length nCount characters from a CHString string, starting at position nFirst (zero-based). The method returns a copy of the extracted substring.
old-location: wmi\chstring_mid.htm
old-project: WmiSdk
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHString.Mid, CHString::Mid, CHString::Mid methods [Windows Management Instrumentation], Mid, chstring/CHString::Mid, wmi.chstring_mid
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
-	DllExport
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString::Mid
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::Mid


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>The <b>Mid</b> method extracts a substring of length <i>nCount</i> characters from a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string, starting at position <i>nFirst</i> (zero-based). The method returns a copy of the extracted substring.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f79f7b70-0587-4d5d-8a18-c61bd3c69212">Mid(int,int)</a>
</td>
<td align="left" width="63%">
Extracts a substring of specified length and beginning point.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfc52075-2323-438e-9fe9-7ca3f2de2e35">Mid(int)</a>
</td>
<td align="left" width="63%">
Extracts a substring beginning at int.

</td>
</tr>
</table>

## -parameters


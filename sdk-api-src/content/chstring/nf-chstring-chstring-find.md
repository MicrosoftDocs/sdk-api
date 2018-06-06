---
UID: NF:chstring.CHString.Find
title: CHString::Find
author: windows-sdk-content
description: The Find method searches a string for the first match of a substring.
old-location: wmi\chstring_find.htm
old-project: WmiSdk
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHString.Find, CHString::Find, CHString::Find methods [Windows Management Instrumentation], Find, chstring/CHString::Find, wmi.chstring_find
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
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString::Find
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::Find


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>The <b>Find</b> method searches a string for the first match of a substring.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f25db53e-f1a2-4b22-98de-b53ccf3952a1">Find(WCHAR)</a>
</td>
<td align="left" width="63%">
Searches for the <b>WSTR</b> in this string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2a8998c-e0e3-47d0-9539-9ae1d1fba5c8">Find(LPCWSTR)</a>
</td>
<td align="left" width="63%">
Searches for the  <b>LPCWSTR</b> in this string.

</td>
</tr>
</table>

## -parameters


---
UID: NF:chstring.CHString.FormatMessageW
title: CHString::FormatMessageW (chstring.h)
author: windows-sdk-content
description: The overloaded FormatMessageW method formats a message string.
old-location: wmi\chstring_formatmessagew.htm
tech.root: WmiSdk
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CHString.FormatMessageW, CHString::FormatMessageW, CHString::FormatMessageW methods [Windows Management Instrumentation], FormatMessageW, chstring/CHString::FormatMessageW, wmi.chstring_formatmessagew
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
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString::FormatMessageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::FormatMessageW


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>The 
overloaded <b>FormatMessageW</b> method formats a message string.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efa2f907-3a83-4508-95ef-5d40513f507e">FormatMessageW(UINT)</a>
</td>
<td align="left" width="63%">
Formats this message according to the resource identifier specified by the <b>UINT</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32200a5e-1fdc-4ca1-bee3-0846da8c22a5">FormatMessageW(LPCWSTR)</a>
</td>
<td align="left" width="63%">
Formats this message string according to the format specified by the <b>LPCWSTR</b>.

</td>
</tr>
</table>

## -parameters


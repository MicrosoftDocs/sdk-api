---
UID: NF:chstring.CHString.Format(UINT,...)
title: CHString::Format(UINT,
author: windows-sdk-content
description: The Format method formats and stores a series of characters and values in a CHString string.
old-location: wmi\chstring_format.htm
old-project: WmiSdk
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHString.Format, CHString.Format(UINT,, CHString::Format, CHString::Format methods [Windows Management Instrumentation], CHString::Format(UINT,, Format, chstring/CHString::Format, wmi.chstring_format
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
-	CHString::Format
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::Format(UINT,


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>The <b>Format</b> method formats and stores a series of characters and values in a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fadf422-fa36-4c68-b150-c79a71346768">Format(UINT)</a>
</td>
<td align="left" width="63%">
Formats this CHString according to the resource identifier specified by the <b>UINT</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2187385b-8e30-4620-be1a-8c95c4d870b1">Format(LPCWSTR)</a>
</td>
<td align="left" width="63%">
Formats this CHString according to the format specified by the <b>LPCWSTR</b>.

</td>
</tr>
</table>

## -parameters


---
UID: NF:chstring.CHString.CHString
title: CHString::CHString
author: windows-sdk-content
description: Each of the following constructors initializes a new CHString object with the specified data.
old-location: wmi\chstring_chstring.htm
old-project: WmiSdk
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHString, CHString.CHString, CHString::CHString, CHString::CHString constructors [Windows Management Instrumentation], chstring/CHString::CHString, wmi.chstring_chstring
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
 - CHString::CHString
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::CHString


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]
<span>Each of the following constructors initializes a new <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object with the specified data.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb7da79b-f808-4f2d-ac33-559fdc9a9978">CHString()</a>
</td>
<td align="left" width="63%">
Creates an empty CHString object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a12cbd2-7fc5-4d82-a85a-dcc1d538a839">CHString(LPCSTR)</a>
</td>
<td align="left" width="63%">
Initializes with the LPCSTR value.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11780ce1-b7d8-4a79-89fc-656ea5d71048">CHString(LPCWSTR)</a>
</td>
<td align="left" width="63%">
Initializes with the LPCWSTR value.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b0afbc0-3ce0-4bcc-8ad1-e3b546d3b0dd">CHString(WCHAR,int)</a>
</td>
<td align="left" width="63%">
Initializes with int copies of the WCHAR value.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58d588fe-6fd4-40c6-83fd-b78e0e409783">CHString(LPCWSTR,int)</a>
</td>
<td align="left" width="63%">
Initializes with int copies of the LPCWSTR value.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b799ee3-e54f-4911-ac0c-4bca91a830d4">CHString(const CHString&)</a>
</td>
<td align="left" width="63%">
Replicates the CHString parameter.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1cf180-bc7c-40ba-91ab-091018790b39">CHString(const unsigned char*)</a>
</td>
<td align="left" width="63%">
Initializes with the value pointed to by char*.

</td>
</tr>
</table>

## -parameters


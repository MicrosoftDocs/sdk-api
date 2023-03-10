---
UID: NF:netfw.INetFwPolicy.GetProfileByType
title: INetFwPolicy::GetProfileByType (netfw.h)
description: Retrieves the profile of the requested type.
helpviewer_keywords: ["GetProfileByType","GetProfileByType method [ICS/ICF]","GetProfileByType method [ICS/ICF]","INetFwPolicy interface","INetFwPolicy interface [ICS/ICF]","GetProfileByType method","INetFwPolicy.GetProfileByType","INetFwPolicy::GetProfileByType","ics.inetfwpolicy_getprofilebytype","netfw/INetFwPolicy::GetProfileByType"]
old-location: ics\inetfwpolicy_getprofilebytype.htm
tech.root: ics
ms.assetid: 4c3876cf-40a4-4315-a87a-8fcdf509d48e
ms.date: 12/05/2018
ms.keywords: GetProfileByType, GetProfileByType method [ICS/ICF], GetProfileByType method [ICS/ICF],INetFwPolicy interface, INetFwPolicy interface [ICS/ICF],GetProfileByType method, INetFwPolicy.GetProfileByType, INetFwPolicy::GetProfileByType, ics.inetfwpolicy_getprofilebytype, netfw/INetFwPolicy::GetProfileByType
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwPolicy::GetProfileByType
 - netfw/INetFwPolicy::GetProfileByType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwPolicy.GetProfileByType
---

# INetFwPolicy::GetProfileByType


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Retrieves the profile of the requested type.

## -parameters

### -param profileType [in]

Type of profile from <a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_profile_type">NET_FW_PROFILE_TYPE</a>.

### -param profile [out, ref]

Retrieved profile of type <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>.

Retrieved profile of type <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>.

## -returns

<h3>C++</h3>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds, the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy">INetFwPolicy</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_profile_type">NET_FW_PROFILE_TYPE</a>
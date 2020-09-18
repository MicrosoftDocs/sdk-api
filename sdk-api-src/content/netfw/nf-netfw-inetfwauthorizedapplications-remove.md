---
UID: NF:netfw.INetFwAuthorizedApplications.Remove
title: INetFwAuthorizedApplications::Remove (netfw.h)
description: The Remove method removes an application from the collection.
helpviewer_keywords: ["INetFwAuthorizedApplications interface [ICS/ICF]","Remove method","INetFwAuthorizedApplications.Remove","INetFwAuthorizedApplications::Remove","Remove","Remove method [ICS/ICF]","Remove method [ICS/ICF]","INetFwAuthorizedApplications interface","ics.inetfwauthorizedapplications_remove","netfw/INetFwAuthorizedApplications::Remove"]
old-location: ics\inetfwauthorizedapplications_remove.htm
tech.root: ics
ms.assetid: 7c4e7d3f-6ab2-46f9-a5a0-f2901a8b5734
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplications interface [ICS/ICF],Remove method, INetFwAuthorizedApplications.Remove, INetFwAuthorizedApplications::Remove, Remove, Remove method [ICS/ICF], Remove method [ICS/ICF],INetFwAuthorizedApplications interface, ics.inetfwauthorizedapplications_remove, netfw/INetFwAuthorizedApplications::Remove
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
 - INetFwAuthorizedApplications::Remove
 - netfw/INetFwAuthorizedApplications::Remove
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
 - INetFwAuthorizedApplications.Remove
---

# INetFwAuthorizedApplications::Remove


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>Remove</b> method removes an application from the collection.

## -parameters

### -param imageFileName [in]

Application name to be removed.

## -returns

<h3>C++</h3>
If the method succeeds the return value is <b>S_OK</b>.

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
</table>
 

<h3>VB</h3>
If the method succeeds the return value is <b>S_OK</b>.

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
</table>

## -remarks

The <b>imageFileName</b> parameter must be a fully qualified path and may contain environment variables.

If the application does not exist in the collection, the Remove method has no effect.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a>
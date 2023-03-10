---
UID: NF:netfw.INetFwAuthorizedApplications.Add
title: INetFwAuthorizedApplications::Add (netfw.h)
description: The Add method adds a new application to the collection.
helpviewer_keywords: ["Add","Add method [ICS/ICF]","Add method [ICS/ICF]","INetFwAuthorizedApplications interface","INetFwAuthorizedApplications interface [ICS/ICF]","Add method","INetFwAuthorizedApplications.Add","INetFwAuthorizedApplications::Add","ics.inetfwauthorizedapplications_add","netfw/INetFwAuthorizedApplications::Add"]
old-location: ics\inetfwauthorizedapplications_add.htm
tech.root: ics
ms.assetid: f69f906d-0d7b-4f45-9bf0-fd1b031e3492
ms.date: 12/05/2018
ms.keywords: Add, Add method [ICS/ICF], Add method [ICS/ICF],INetFwAuthorizedApplications interface, INetFwAuthorizedApplications interface [ICS/ICF],Add method, INetFwAuthorizedApplications.Add, INetFwAuthorizedApplications::Add, ics.inetfwauthorizedapplications_add, netfw/INetFwAuthorizedApplications::Add
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
 - INetFwAuthorizedApplications::Add
 - netfw/INetFwAuthorizedApplications::Add
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
 - INetFwAuthorizedApplications.Add
---

# INetFwAuthorizedApplications::Add


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>Add</b> method adds a new application to the collection.

## -parameters

### -param app [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
Application to add to the collection via an <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFWAuthorizedApplication</a> object.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
Application to add to the collection via an <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFWAuthorizedApplication</a> object. 

</td>
</tr>
</table>

## -returns

<h3>C++</h3>
If the method succeeds the return value is S_OK.

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
The method failed because a parameter was not valid.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The  method failed because the  object is already in the collection.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds the return value is S_OK.

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
The method failed because a parameter was not valid.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The  method failed because the  object is already in the collection.

</td>
</tr>
</table>

## -remarks

If an application with the same path already exists, the existing settings are overwritten.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFWAuthorizedApplication</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a>
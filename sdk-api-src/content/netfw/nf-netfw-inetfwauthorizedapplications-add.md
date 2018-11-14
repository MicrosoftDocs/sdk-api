---
UID: NF:netfw.INetFwAuthorizedApplications.Add
title: INetFwAuthorizedApplications::Add
author: windows-sdk-content
description: The Add method adds a new application to the collection.
old-location: ics\inetfwauthorizedapplications_add.htm
tech.root: ICS
ms.assetid: f69f906d-0d7b-4f45-9bf0-fd1b031e3492
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Add, Add method [ICS/ICF], Add method [ICS/ICF],INetFwAuthorizedApplications interface, INetFwAuthorizedApplications interface [ICS/ICF],Add method, INetFwAuthorizedApplications.Add, INetFwAuthorizedApplications::Add, ics.inetfwauthorizedapplications_add, netfw/INetFwAuthorizedApplications::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netfw.h
: 
- INetFwAuthorizedApplications.Add
: 
---

# INetFwAuthorizedApplications::Add


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>Add</b> method adds a new application to the collection.


## -parameters




### -param app

TBD




#### - application [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
Application to add to the collection via an <a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFWAuthorizedApplication</a> object.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
Application to add to the collection via an <a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFWAuthorizedApplication</a> object. 

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




<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFWAuthorizedApplication</a>



<a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFwAuthorizedApplications</a>
 

 


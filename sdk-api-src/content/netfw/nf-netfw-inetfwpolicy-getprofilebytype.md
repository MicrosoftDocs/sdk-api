---
UID: NF:netfw.INetFwPolicy.GetProfileByType
title: INetFwPolicy::GetProfileByType
author: windows-sdk-content
description: Retrieves the profile of the requested type.
old-location: ics\inetfwpolicy_getprofilebytype.htm
tech.root: ICS
ms.assetid: 4c3876cf-40a4-4315-a87a-8fcdf509d48e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProfileByType, GetProfileByType method [ICS/ICF], GetProfileByType method [ICS/ICF],INetFwPolicy interface, INetFwPolicy interface [ICS/ICF],GetProfileByType method, INetFwPolicy.GetProfileByType, INetFwPolicy::GetProfileByType, ics.inetfwpolicy_getprofilebytype, netfw/INetFwPolicy::GetProfileByType
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
 - INetFwPolicy.GetProfileByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwPolicy::GetProfileByType


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Retrieves the profile of the requested type. 


## -parameters




### -param profileType [in]

Type of profile from <a href="https://msdn.microsoft.com/abf59405-86c7-4a20-a3e9-b12b27290b00">NET_FW_PROFILE_TYPE</a>.


### -param profile [out, ref]

Retrieved profile of type <a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>.

Retrieved profile of type <a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>.


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




<a href="https://msdn.microsoft.com/8bfe55b6-c38d-47f8-9160-a304a85eb67f">INetFwPolicy</a>



<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>



<a href="https://msdn.microsoft.com/abf59405-86c7-4a20-a3e9-b12b27290b00">NET_FW_PROFILE_TYPE</a>
 

 


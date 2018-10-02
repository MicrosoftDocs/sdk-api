---
UID: NF:netfw.INetFwAuthorizedApplications.Item
title: INetFwAuthorizedApplications::Item
author: windows-sdk-content
description: The Item method returns the specified application if it is in the collection.
old-location: ics\inetfwauthorizedapplications_item.htm
tech.root: ICS
ms.assetid: 3c9eac16-9ba5-43f6-b52e-4340598745d8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetFwAuthorizedApplications interface [ICS/ICF],Item method, INetFwAuthorizedApplications.Item, INetFwAuthorizedApplications::Item, Item, Item method [ICS/ICF], Item method [ICS/ICF],INetFwAuthorizedApplications interface, ics.inetfwauthorizedapplications_item, netfw/INetFwAuthorizedApplications::Item
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
 - INetFwAuthorizedApplications.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwAuthorizedApplications::Item


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>Item</b> method returns the specified application if it is in the collection.


## -parameters




### -param imageFileName [in]

Application to retrieve.


### -param app

TBD




#### - String imageFileName [in]

Application to retrieve.


#### - application [out]

Reference to the returned <a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a> object.

Reference to the returned <a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a> object.


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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) </b></dt>
</dl>
</td>
<td width="60%">
The requested item does not exist.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) </b></dt>
</dl>
</td>
<td width="60%">
The requested item does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a>



<a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFwAuthorizedApplications</a>
 

 


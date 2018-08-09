---
UID: NF:netlistmgr.INetworkCostManager.SetDestinationAddresses
title: INetworkCostManager::SetDestinationAddresses
author: windows-sdk-content
description: SetDestinationAddresses method registers specified destination IPv4/IPv6 addresses to receive cost or data plan status change notifications.
old-location: nla\inetworkcostmanager_setdestinationaddresses.htm
old-project: nla
ms.assetid: D4CA45C5-0AF1-443A-9134-BB82268ABFD5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INetworkCostManager interface [Network Awareness],SetDestinationAddresses method, INetworkCostManager.SetDestinationAddresses, INetworkCostManager::SetDestinationAddresses, SetDestinationAddresses, SetDestinationAddresses method [Network Awareness], SetDestinationAddresses method [Network Awareness],INetworkCostManager interface, netlistmgr/INetworkCostManager::SetDestinationAddresses, nla.inetworkcostmanager_setdestinationaddresses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkCostManager.SetDestinationAddresses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkCostManager::SetDestinationAddresses


## -description


The <b>SetDestinationAddresses</b> method registers specified destination IPv4/IPv6 addresses to receive cost or data plan status change notifications.


## -parameters




### -param length [in]

The number of destination IPv4/IPv6 addresses in the list.


### -param pDestIPAddrList [in]

A <a href="https://msdn.microsoft.com/BEAF672C-F9B3-4544-878B-BBCF96F502C6">NLM_SOCKADDR</a> structure containing a list of destination IPv4/IPv6 addresses to register for cost or data plan status change notification.


### -param bAppend

If true, <i>pDestIPAddrList</i> will be appended to the existing address list; otherwise the existing list will be overwritten.


## -returns



Returns S_OK on success, otherwise an HRESULT error code is returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Returned if one of the following occurs:

<ul>
<li><i>length</i> is 0.</li>
<li><i>length</i> is larger than NLM_MAX_ADDRESS_LIST_SIZE(10)</li>
<li><i>bAppend</i> is VARIANT_TRUE, but including the number of subscribed destinations in the existing list with the value of <i>length</i> exceeds NLM_MAX_ADDRESS_SIZE.</li>
<li>A destination address in the supplied list is invalid.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>destIPAddrList</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if either an IPv4 or IPv6 stack is not present on the local computer but  either an IPv4 or IPv6 address was specified by<i>destIPAddr</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
This method was called after registering for <a href="https://msdn.microsoft.com/A8F4194E-6E9A-4173-8F88-FC2923B11CF0">INetworkCostManagerEvents</a> by calling <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a>. See Remark for more information.

</td>
</tr>
</table>
 




## -remarks



This method must be called before <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a>. Once <b>IConnectionPoint::Advise</b> is called, this method will not complete successfully until last sink calls <a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">IConnectionPoint::UnAdvise</a>. However, this method can be called multiple times prior to the call to<b>IConnectionPoint::Advise</b>.

 If a list of destination addresses indicated by <i>pDestIPAddrList</i>  contains duplicate addresses, only one of each will be used to notify cost changes. Callers can clear a list of destinations by calling this function with <i>length</i> set to 0, <i>destIPAddrList</i> set NULL, and <i>bAppend</i> set FALSE.




## -see-also




<a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a>



<a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">IConnectionPoint::UnAdvise</a>



<a href="https://msdn.microsoft.com/A6316E94-398D-4D87-B631-6BEF416895EE">INetworkCostManager</a>
 

 


---
UID: NF:iphlpapi.CancelIPChangeNotify
title: CancelIPChangeNotify function
author: windows-sdk-content
description: Cancels notification of IPv4 address and route changes previously requested with successful calls to the NotifyAddrChange or NotifyRouteChange functions.
old-location: iphlp\cancelipchangenotify.htm
old-project: iphlp
ms.assetid: 10795401-003f-45ce-80f1-ccc31659298a
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CancelIPChangeNotify, CancelIPChangeNotify function [IP Helper], iphlp.cancelipchangenotify, iphlpapi/CancelIPChangeNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CancelIPChangeNotify
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# CancelIPChangeNotify function


## -description


The <b>CancelIPChangeNotify</b> function cancels notification of IPv4 address and route changes previously requested with successful calls to the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a> functions.


## -parameters




### -param notifyOverlapped [in]

A pointer to the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure used in the previous call to <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>  or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a>.


## -remarks



The  
<b>CancelIPChangeNotify</b> function deregisters for a change notification previously requested for IPv4 address or route changes on  a local computer. These requests to register for notification are made  by calling the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a> functions.  

The <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure used in the previous call to one of these notification functions is passed to <b>CancelIPChangeNotify</b> function in the <i>notifyOverlapped</i> parameter to deregister for notifications.

The <b>CancelIPChangeNotify</b> can return <b>FALSE</b> if no notification request was found or an invalid <i>notifyOverlapped</i> parameter was passed. 




## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>



<a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 


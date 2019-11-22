---
UID: NF:iphlpapi.CancelIPChangeNotify
title: CancelIPChangeNotify function (iphlpapi.h)

description: Cancels notification of IPv4 address and route changes previously requested with successful calls to the NotifyAddrChange or NotifyRouteChange functions.
old-location: iphlp\cancelipchangenotify.htm
tech.root: IpHlp
ms.assetid: 10795401-003f-45ce-80f1-ccc31659298a

ms.date: 12/05/2018
ms.keywords: CancelIPChangeNotify, CancelIPChangeNotify function [IP Helper], iphlp.cancelipchangenotify, iphlpapi/CancelIPChangeNotify
ms.topic: function
f1_keywords:
- iphlpapi/CancelIPChangeNotify
dev_langs:
 - c++
req.header: iphlpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iphlpapi.dll
api_name:
- CancelIPChangeNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CancelIPChangeNotify function


## -description


The <b>CancelIPChangeNotify</b> function cancels notification of IPv4 address and route changes previously requested with successful calls to the <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a> or <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a> functions.


## -parameters




### -param notifyOverlapped [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure used in the previous call to <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a>  or <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a>.


## -remarks



The  
<b>CancelIPChangeNotify</b> function deregisters for a change notification previously requested for IPv4 address or route changes on  a local computer. These requests to register for notification are made  by calling the <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a> or <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a> functions.  

The <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure used in the previous call to one of these notification functions is passed to <b>CancelIPChangeNotify</b> function in the <i>notifyOverlapped</i> parameter to deregister for notifications.

The <b>CancelIPChangeNotify</b> can return <b>FALSE</b> if no notification request was found or an invalid <i>notifyOverlapped</i> parameter was passed. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyroutechange">NotifyRouteChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>
 

 


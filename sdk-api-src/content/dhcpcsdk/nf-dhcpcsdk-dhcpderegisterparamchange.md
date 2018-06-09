---
UID: NF:dhcpcsdk.DhcpDeRegisterParamChange
title: DhcpDeRegisterParamChange function
author: windows-sdk-content
description: The DhcpDeRegisterParamChange function releases resources associated with previously registered event notifications, and closes the associated event handle.
old-location: dhcp\dhcpderegisterparamchange.htm
old-project: DHCP
ms.assetid: a3fa7c45-cad3-43be-a6c1-fffe6d025d95
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DhcpDeRegisterParamChange, DhcpDeRegisterParamChange function [DHCP], _dhcp_dhcpderegisterparamchange, dhcp.dhcpderegisterparamchange, dhcpcsdk/DhcpDeRegisterParamChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: KSJACK_DESCRIPTION, *PKSJACK_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpDeRegisterParamChange
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
---

# DhcpDeRegisterParamChange function


## -description


The 
<b>DhcpDeRegisterParamChange</b> function releases resources associated with previously registered event notifications, and closes the associated event handle.


## -parameters




### -param Flags [in]

Reserved. Must be set to zero.


### -param Reserved [in]

Reserved. Must be set to <b>NULL</b>.


### -param Event [in]

Must be the same value as the <b>HANDLE</b> variable in the 
<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a> function call for which the client is deregistering event notification.


## -returns



Returns ERROR_SUCCESS upon successful completion. Otherwise, returns Windows error codes.




## -remarks



The 
<b>DhcpDeRegisterParamChange</b> function must be made subsequent to an associated 
<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a> function call, and the <i>Flags</i> parameter and the <b>HANDLE</b> variable passed  
in the <i>Event</i> parameter to <b>DhcpDeRegisterParamChange</b> must match corresponding <i>Flags</i> parameter and the <b>HANDLE</b> variable of the previous and associated 
<b>DhcpRegisterParamChange</b> function call.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a>



<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a>
 

 


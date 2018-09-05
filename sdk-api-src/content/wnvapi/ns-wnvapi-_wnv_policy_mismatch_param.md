---
UID: NS:wnvapi._WNV_POLICY_MISMATCH_PARAM
title: "_WNV_POLICY_MISMATCH_PARAM"
author: windows-sdk-content
description: Specifies the parameters of an event (typically an incoming packet) that causes the Windows Network Virtualization (WNV) driver to generate a WnvPolicyMismatchType notification.
old-location: wnv\wnv_policy_mismatch_param.htm
old-project: wnv
ms.assetid: 2781B0D6-950E-49AD-9B30-31DE4A27ED4A
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWNV_POLICY_MISMATCH_PARAM, PWNV_POLICY_MISMATCH_PARAM, PWNV_POLICY_MISMATCH_PARAM structure pointer [Windows Network Virtualization], WNV_POLICY_MISMATCH_PARAM, WNV_POLICY_MISMATCH_PARAM structure [Windows Network Virtualization], _WNV_POLICY_MISMATCH_PARAM, wnv.wnv_policy_mismatch_param, wnvapi/PWNV_POLICY_MISMATCH_PARAM, wnvapi/WNV_POLICY_MISMATCH_PARAM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wnvapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WNV_POLICY_MISMATCH_PARAM, *PWNV_POLICY_MISMATCH_PARAM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_POLICY_MISMATCH_PARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNV_POLICY_MISMATCH_PARAM structure


## -description


Specifies the parameters of an event (typically an incoming packet) that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvPolicyMismatchType</b> notification. As a result, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <a href="https://msdn.microsoft.com/CA0F9AAE-95E5-4A62-8A26-11F933B2D09E">WnvRequestNotification</a> function call.


## -struct-fields




### -field CAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the customer address.


### -field PAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the provider address.


### -field VirtualSubnetId

Type: <b>ULONG</b>

The identifier of a customer virtual subnet. This value ranges from 4096 (0x00001000) to 16777214 (0x00FFFFFE).


### -field CA

Type: <b><a href="https://msdn.microsoft.com/1FD137B6-74F4-4E75-A77E-65F093938662">WNV_IP_ADDRESS</a></b>

The IP address object for the customer address, which is the IP address configured on the virtual machine for network virtualization.


### -field PA

Type: <b><a href="https://msdn.microsoft.com/1FD137B6-74F4-4E75-A77E-65F093938662">WNV_IP_ADDRESS</a></b>

The IP address object for the provider address, which is the matching IP address used on the physical network for the customer address.


## -remarks



For a detailed description of network virtualization concepts and terminology, see <a href="http://go.microsoft.com/fwlink/p/?linkid=263545">Hyper-V Network Virtualization Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a>
 

 


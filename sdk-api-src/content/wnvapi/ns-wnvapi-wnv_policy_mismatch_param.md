---
UID: NS:wnvapi._WNV_POLICY_MISMATCH_PARAM
title: WNV_POLICY_MISMATCH_PARAM (wnvapi.h)
description: Specifies the parameters of an event (typically an incoming packet) that causes the Windows Network Virtualization (WNV) driver to generate a WnvPolicyMismatchType notification.
helpviewer_keywords: ["*PWNV_POLICY_MISMATCH_PARAM","PWNV_POLICY_MISMATCH_PARAM","PWNV_POLICY_MISMATCH_PARAM structure pointer [Windows Network Virtualization]","WNV_POLICY_MISMATCH_PARAM","WNV_POLICY_MISMATCH_PARAM structure [Windows Network Virtualization]","wnv.wnv_policy_mismatch_param","wnvapi/PWNV_POLICY_MISMATCH_PARAM","wnvapi/WNV_POLICY_MISMATCH_PARAM"]
old-location: wnv\wnv_policy_mismatch_param.htm
tech.root: wnv
ms.assetid: 2781B0D6-950E-49AD-9B30-31DE4A27ED4A
ms.date: 12/05/2018
ms.keywords: '*PWNV_POLICY_MISMATCH_PARAM, PWNV_POLICY_MISMATCH_PARAM, PWNV_POLICY_MISMATCH_PARAM structure pointer [Windows Network Virtualization], WNV_POLICY_MISMATCH_PARAM, WNV_POLICY_MISMATCH_PARAM structure [Windows Network Virtualization], wnv.wnv_policy_mismatch_param, wnvapi/PWNV_POLICY_MISMATCH_PARAM, wnvapi/WNV_POLICY_MISMATCH_PARAM'
req.header: wnvapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WNV_POLICY_MISMATCH_PARAM, *PWNV_POLICY_MISMATCH_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_POLICY_MISMATCH_PARAM
 - wnvapi/_WNV_POLICY_MISMATCH_PARAM
 - PWNV_POLICY_MISMATCH_PARAM
 - wnvapi/PWNV_POLICY_MISMATCH_PARAM
 - WNV_POLICY_MISMATCH_PARAM
 - wnvapi/WNV_POLICY_MISMATCH_PARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_POLICY_MISMATCH_PARAM
---

# WNV_POLICY_MISMATCH_PARAM structure


## -description

Specifies the parameters of an event (typically an incoming packet) that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvPolicyMismatchType</b> notification. As a result, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function call.

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

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The IP address object for the customer address, which is the IP address configured on the virtual machine for network virtualization.

### -field PA

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The IP address object for the provider address, which is the matching IP address used on the physical network for the customer address.

## -remarks

For a detailed description of network virtualization concepts and terminology, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134230(v=ws.11)">Hyper-V Network Virtualization Overview</a>.

## -see-also

<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a>
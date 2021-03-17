---
UID: NS:wnvapi._WNV_REDIRECT_PARAM
title: WNV_REDIRECT_PARAM (wnvapi.h)
description: Specifies the parameters of the event (receiving an incoming Internet Control Message Protocol redirect packet) that causes the Windows Network Virtualization (WNV) driver to generate a WnvRedirectType notification.
helpviewer_keywords: ["*PWNV_REDIRECT_PARAM","PWNV_REDIRECT_PARAM","PWNV_REDIRECT_PARAM structure pointer [Windows Network Virtualization]","WNV_REDIRECT_PARAM","WNV_REDIRECT_PARAM structure [Windows Network Virtualization]","wnv.wnv_redirect_param","wnvapi/PWNV_REDIRECT_PARAM","wnvapi/WNV_REDIRECT_PARAM"]
old-location: wnv\wnv_redirect_param.htm
tech.root: wnv
ms.assetid: 53305594-4539-490E-B034-99355265F175
ms.date: 12/05/2018
ms.keywords: '*PWNV_REDIRECT_PARAM, PWNV_REDIRECT_PARAM, PWNV_REDIRECT_PARAM structure pointer [Windows Network Virtualization], WNV_REDIRECT_PARAM, WNV_REDIRECT_PARAM structure [Windows Network Virtualization], wnv.wnv_redirect_param, wnvapi/PWNV_REDIRECT_PARAM, wnvapi/WNV_REDIRECT_PARAM'
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
req.typenames: WNV_REDIRECT_PARAM, *PWNV_REDIRECT_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_REDIRECT_PARAM
 - wnvapi/_WNV_REDIRECT_PARAM
 - PWNV_REDIRECT_PARAM
 - wnvapi/PWNV_REDIRECT_PARAM
 - WNV_REDIRECT_PARAM
 - wnvapi/WNV_REDIRECT_PARAM
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
 - WNV_REDIRECT_PARAM
---

# WNV_REDIRECT_PARAM structure


## -description

Specifies the parameters of the event (receiving an incoming Internet Control Message Protocol
redirect packet) that causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvRedirectType</b> notification. If there is a pending call to the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function of this type, the WNV driver fills the buffer that is passed in the <i>NotificationParam</i> argument's <a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure with one or more instances of this structure and completes the <b>WnvRequestNotification</b> function call.

## -struct-fields

### -field CAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the customer address.

### -field PAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the original provider address.

### -field NewPAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the new provider address.

### -field VirtualSubnetId

Type: <b>ULONG</b>

The identifier of a customer virtual subnet. This value ranges from 4096 (0x00001000) to 16777214 (0x00FFFFFE).

### -field CA

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The IP address object for the customer address, which is the IP address configured on the virtual machine for network virtualization.

### -field PA

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The IP address object for the provider address, which is the matching IP address used on the physical network for the customer address.

### -field NewPA

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The updated provider address when a virtual machine is migrated from one host to another.

## -remarks

Hyper-V Network Virtualization uses an Internet Control Message Protocol
(ICMP) redirect message to indicate a change in the virtual machine's provider address in the case of a live migration of a virtual machine.

For a detailed description of network virtualization concepts and terminology, refer to <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134230(v=ws.11)">Hyper-V Network Virtualization Overview</a>.

## -see-also

<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a>
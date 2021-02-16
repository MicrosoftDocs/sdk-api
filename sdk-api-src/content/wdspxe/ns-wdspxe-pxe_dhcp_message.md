---
UID: NS:wdspxe.tagPXE_DHCP_MESSAGE
title: PXE_DHCP_MESSAGE (wdspxe.h)
description: The PXE_DHCP_MESSAGE structure can be used with the Windows Deployment Services PXE Server API.
helpviewer_keywords: ["*PPXE_DHCP_MESSAGE","PPXE_DHCP_MESSAGE","PPXE_DHCP_MESSAGE structure pointer [Windows Deployment Services]","PXE_DHCP_MESSAGE","PXE_DHCP_MESSAGE structure [Windows Deployment Services]","wds.pxe_dhcp_message","wdspxe/PPXE_DHCP_MESSAGE","wdspxe/PXE_DHCP_MESSAGE"]
old-location: wds\pxe_dhcp_message.htm
tech.root: wds
ms.assetid: 466906f1-9439-4c9f-91f1-28530969181c
ms.date: 12/05/2018
ms.keywords: '*PPXE_DHCP_MESSAGE, PPXE_DHCP_MESSAGE, PPXE_DHCP_MESSAGE structure pointer [Windows Deployment Services], PXE_DHCP_MESSAGE, PXE_DHCP_MESSAGE structure [Windows Deployment Services], wds.pxe_dhcp_message, wdspxe/PPXE_DHCP_MESSAGE, wdspxe/PXE_DHCP_MESSAGE'
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: PXE_DHCP_MESSAGE, *PPXE_DHCP_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_DHCP_MESSAGE
 - wdspxe/tagPXE_DHCP_MESSAGE
 - PPXE_DHCP_MESSAGE
 - wdspxe/PPXE_DHCP_MESSAGE
 - PXE_DHCP_MESSAGE
 - wdspxe/PXE_DHCP_MESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_DHCP_MESSAGE
---

# PXE_DHCP_MESSAGE structure


## -description

The <b>PXE_DHCP_MESSAGE</b> structure can be used with the Windows Deployment Services PXE Server API.

## -struct-fields

### -field Operation

Operation (op) field

### -field HardwareAddressType

Hardware Address Type (htype) field

### -field HardwareAddressLength

Hardware Address Length (hlen) field

### -field HopCount

### -field TransactionID

### -field SecondsSinceBoot

Seconds Since Boot (secs) field

### -field Reserved

This parameter is reserved.

### -field ClientIpAddress

Client IP Address (ciaddr) field

### -field YourIpAddress

### -field BootstrapServerAddress

### -field RelayAgentIpAddress

### -field HardwareAddress

### -field HostName

### -field BootFileName

### -field bMagicCookie

### -field uMagicCookie

### -field Option

### -field YourIPAddress

Your IP Address (yiaddr) field


---
UID: NF:wdspxe.PxeDhcpAppendOption
title: PxeDhcpAppendOption function (wdspxe.h)
description: Appends a DHCP option to the reply packet. (PxeDhcpAppendOption)
helpviewer_keywords: ["PxeDhcpAppendOption","PxeDhcpAppendOption function [Windows Deployment Services]","wds.pxedhcpappendoption","wdspxe/PxeDhcpAppendOption"]
old-location: wds\pxedhcpappendoption.htm
tech.root: wds
ms.assetid: bc639af6-de51-4c82-985a-96e5a10389e7
ms.date: 12/05/2018
ms.keywords: PxeDhcpAppendOption, PxeDhcpAppendOption function [Windows Deployment Services], wds.pxedhcpappendoption, wdspxe/PxeDhcpAppendOption
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
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeDhcpAppendOption
 - wdspxe/PxeDhcpAppendOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpAppendOption
---

# PxeDhcpAppendOption function


## -description

Appends a DHCP option to the reply packet.

## -parameters

### -param pReplyPacket [in, out]

Pointer to a reply packet allocated with the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

### -param uMaxReplyPacketLen [in]

Allocated length of the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param puReplyPacketLen [in, out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param bOption [in]

DHCP option to add to the packet.

### -param bOptionLen [in]

Length of the option value pointed to by the <i>pValue</i> parameter. This parameter is 
      ignored if the <i>bOption</i> parameter is End Option (0xFF) or Pad Option (0x00).

### -param pValue [in]

Address of the buffer that contains the DHCP option value. This parameter is ignored if the 
      <i>bOption</i> parameter is End Option (0xFF) or Pad Option (0x00).

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>

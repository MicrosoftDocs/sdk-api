---
UID: NF:wdspxe.PxeDhcpv6AppendOptionRaw
title: PxeDhcpv6AppendOptionRaw function (wdspxe.h)
author: windows-sdk-content
description: Appends a DHCPv6 option to the reply packet.
old-location: wds\pxedhcpv6appendoptionraw.htm
tech.root: wds
ms.assetid: DABE18C2-50C3-4923-A2C9-8382DF762D3F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PxeDhcpv6AppendOptionRaw, PxeDhcpv6AppendOptionRaw function [Windows Deployment Services], wds.pxedhcpv6appendoptionraw, wdspxe/PxeDhcpv6AppendOptionRaw
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6AppendOptionRaw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxeDhcpv6AppendOptionRaw function


## -description


Appends a DHCPv6 option to the reply packet.


## -parameters




### -param pReply [in, out]

Pointer to a reply packet allocated with the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.


### -param cbReply [in]

Allocated length of the packet pointed to by the <i>pReply</i> parameter.


### -param pcbReplyUsed [in, out]

On entry, this is the number of bytes of the buffer pointed to by <i>pReply</i> that are currently used.  On success of the function, this is updated to the number of bytes used after appending the option.


### -param cbBuffer [in]

Length of the option value pointed to by the <i>pBuffer</i> parameter. 


### -param pBuffer [in]

Address of the buffer that contains the DHCPv6 option value. The buffer must contain the encoded option code and option size.

For more information about encoding the option code and option size, developers should refer to the Dynamic Host Configuration Protocol for IPv6 <a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a> maintained by The Internet Engineering Task Force (IETF).


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
 

 


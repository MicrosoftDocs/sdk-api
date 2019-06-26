---
UID: NF:wdspxe.PxeDhcpAppendOptionRaw
title: PxeDhcpAppendOptionRaw function (wdspxe.h)
author: windows-sdk-content
description: Appends a DHCP option to the reply packet.
old-location: wds\pxedhcpappendoptionraw.htm
tech.root: wds
ms.assetid: f6525a06-a3b0-4989-8132-fa8f1ad2fec3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PxeDhcpAppendOptionRaw, PxeDhcpAppendOptionRaw function [Windows Deployment Services], wds.pxedhcpappendoptionraw, wdspxe/PxeDhcpAppendOptionRaw
ms.topic: function
f1_keywords: 
 - "wdspxe/PxeDhcpAppendOptionRaw"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpAppendOptionRaw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxeDhcpAppendOptionRaw function


## -description


Appends a DHCP option to the reply packet.


## -parameters




### -param pReplyPacket [in, out]

Pointer to a reply packet allocated with the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.


### -param uMaxReplyPacketLen [in]

Allocated length of the packet pointed to by the <i>pReplyPacket</i> parameter.


### -param puReplyPacketLen [in, out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReplyPacket</i> parameter.


### -param uBufferLen [in]

Length of the option value pointed to by the <i>pBuffer</i> parameter. 


### -param pBuffer [in]

Address of the buffer that contains the DHCP option value. 


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
 

 


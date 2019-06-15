---
UID: NF:wdspxe.PxeSendReply
title: PxeSendReply function (wdspxe.h)
author: windows-sdk-content
description: Sends a packet to a client request.
old-location: wds\pxesendreply.htm
tech.root: wds
ms.assetid: b4809f0b-b8a5-45d1-b6ef-8f812379e706
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PxeSendReply, PxeSendReply function [Windows Deployment Services], wds.pxesendreply, wdspxe/PxeSendReply
ms.topic: function
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
 - PxeSendReply
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxeSendReply function


## -description


Sends a packet to a client request.


## -parameters




### -param hClientRequest [in]

Handle to the client request received in the 
      <a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> callback.


### -param pPacket [in]

Pointer to packet allocated by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.


### -param uPacketLen [in]

Length of the packet pointed to by the <i>pPacket</i> parameter.


### -param pAddress [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/ns-wdspxe-tagpxe_address">PXE_ADDRESS</a> structure that contains the 
      destination address of the packet. If the <i>pAddress</i> parameter is 
      <b>NULL</b>, then the packet is sent to the source address of the client request.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/ns-wdspxe-tagpxe_address">PXE_ADDRESS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
 

 


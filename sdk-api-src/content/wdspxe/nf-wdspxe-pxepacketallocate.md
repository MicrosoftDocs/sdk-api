---
UID: NF:wdspxe.PxePacketAllocate
title: PxePacketAllocate function (wdspxe.h)
description: Allocates a packet to be sent with the PxeSendReply function.
helpviewer_keywords: ["PxePacketAllocate","PxePacketAllocate function [Windows Deployment Services]","wds.pxepacketallocate","wdspxe/PxePacketAllocate"]
old-location: wds\pxepacketallocate.htm
tech.root: wds
ms.assetid: f3a664a8-565c-4894-bea7-6664df0ecd9b
ms.date: 12/05/2018
ms.keywords: PxePacketAllocate, PxePacketAllocate function [Windows Deployment Services], wds.pxepacketallocate, wdspxe/PxePacketAllocate
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
 - PxePacketAllocate
 - wdspxe/PxePacketAllocate
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
 - PxePacketAllocate
---

# PxePacketAllocate function


## -description

Allocates a packet to be sent with the 
    <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a> function.

## -parameters

### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function.

### -param hClientRequest [in]

Handle to the client request received in the 
      <a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> callback.

### -param uSize [in]

Size of the buffer to be allocated.

## -returns

Address of allocated buffer, or <b>NULL</b> if the allocation failed. For extended error 
      information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketfree">PxePacketFree</a>



<a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a>



<a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
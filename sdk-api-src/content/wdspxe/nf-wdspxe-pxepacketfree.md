---
UID: NF:wdspxe.PxePacketFree
title: PxePacketFree function (wdspxe.h)
description: Frees a packet allocated by the PxePacketAllocate function.
helpviewer_keywords: ["PxePacketFree","PxePacketFree function [Windows Deployment Services]","wds.pxepacketfree","wdspxe/PxePacketFree"]
old-location: wds\pxepacketfree.htm
tech.root: wds
ms.assetid: de93d42d-9c46-4944-a6e9-5dd72b8a3278
ms.date: 12/05/2018
ms.keywords: PxePacketFree, PxePacketFree function [Windows Deployment Services], wds.pxepacketfree, wdspxe/PxePacketFree
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
 - PxePacketFree
 - wdspxe/PxePacketFree
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
 - PxePacketFree
---

# PxePacketFree function


## -description

Frees a packet allocated by the 
    <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

## -parameters

### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function.

### -param hClientRequest [in]

Handle to the client request received in the 
      <a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> callback.

### -param pPacket [in]

Pointer to packet allocated by the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a>



<a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
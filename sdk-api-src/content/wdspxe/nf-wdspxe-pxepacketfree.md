---
UID: NF:wdspxe.PxePacketFree
title: PxePacketFree function (wdspxe.h)
author: windows-sdk-content
description: Frees a packet allocated by the PxePacketAllocate function.
old-location: wds\pxepacketfree.htm
tech.root: wds
ms.assetid: de93d42d-9c46-4944-a6e9-5dd72b8a3278
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PxePacketFree, PxePacketFree function [Windows Deployment Services], wds.pxepacketfree, wdspxe/PxePacketFree
ms.topic: function
f1_keywords: 
 - "wdspxe/PxePacketFree"
dev_langs:
 - c++
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
 - PxePacketFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxePacketFree function


## -description


Frees a packet allocated by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.


## -parameters




### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function.


### -param hClientRequest [in]

Handle to the client request received in the 
      <a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> callback.


### -param pPacket [in]

Pointer to packet allocated by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
 

 


---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.GetDesktopSharedRect
title: IRDPSRAPISharingSession::GetDesktopSharedRect
author: windows-sdk-content
description: Retrieves the current desktop region being shared.
old-location: rdp\irdpsrapisharingsession_getdesktopsharedrect.htm
old-project: Rdp
ms.assetid: 2b224fa2-928d-4222-80a6-91f654b97ae1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetDesktopSharedRect, GetDesktopSharedRect method [RDP], GetDesktopSharedRect method [RDP],IRDPSRAPISharingSession interface, GetDesktopSharedRect method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],GetDesktopSharedRect method, IRDPSRAPISharingSession.GetDesktopSharedRect, IRDPSRAPISharingSession2 interface [RDP],GetDesktopSharedRect method, IRDPSRAPISharingSession2::GetDesktopSharedRect, IRDPSRAPISharingSession::GetDesktopSharedRect, rdp.irdpsrapisharingsession_getdesktopsharedrect, rdpencomapi/IRDPSRAPISharingSession2::GetDesktopSharedRect, rdpencomapi/IRDPSRAPISharingSession::GetDesktopSharedRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPISharingSession2.GetDesktopSharedRect
 - IRDPSRAPISharingSession.GetDesktopSharedRect
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPISharingSession::GetDesktopSharedRect


## -description


Retrieves the current desktop region being shared.


## -parameters




### -param pleft




### -param ptop




### -param pright




### -param pbottom






#### - bottom [out]

Type: <b>long*</b>

Y-coordinate of the lower-right corner of the shared rectangle.


#### - left [out]

Type: <b>long*</b>

X-coordinate of the upper-left corner of the shared rectangle.


#### - right [out]

Type: <b>long*</b>

X-coordinate of the lower-right corner of the shared rectangle.


#### - top [out]

Type: <b>long*</b>

Y-coordinate of the upper-left corner of the shared rectangle.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>



<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 


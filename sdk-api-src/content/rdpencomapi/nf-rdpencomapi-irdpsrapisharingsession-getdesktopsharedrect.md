---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.GetDesktopSharedRect
title: IRDPSRAPISharingSession::GetDesktopSharedRect (rdpencomapi.h)
description: Retrieves the current desktop region being shared.
helpviewer_keywords: ["GetDesktopSharedRect","GetDesktopSharedRect method [RDP]","GetDesktopSharedRect method [RDP]","IRDPSRAPISharingSession interface","GetDesktopSharedRect method [RDP]","IRDPSRAPISharingSession2 interface","IRDPSRAPISharingSession interface [RDP]","GetDesktopSharedRect method","IRDPSRAPISharingSession.GetDesktopSharedRect","IRDPSRAPISharingSession2 interface [RDP]","GetDesktopSharedRect method","IRDPSRAPISharingSession2::GetDesktopSharedRect","IRDPSRAPISharingSession::GetDesktopSharedRect","rdp.irdpsrapisharingsession_getdesktopsharedrect","rdpencomapi/IRDPSRAPISharingSession2::GetDesktopSharedRect","rdpencomapi/IRDPSRAPISharingSession::GetDesktopSharedRect"]
old-location: rdp\irdpsrapisharingsession_getdesktopsharedrect.htm
tech.root: rdp
ms.assetid: 2b224fa2-928d-4222-80a6-91f654b97ae1
ms.date: 12/05/2018
ms.keywords: GetDesktopSharedRect, GetDesktopSharedRect method [RDP], GetDesktopSharedRect method [RDP],IRDPSRAPISharingSession interface, GetDesktopSharedRect method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],GetDesktopSharedRect method, IRDPSRAPISharingSession.GetDesktopSharedRect, IRDPSRAPISharingSession2 interface [RDP],GetDesktopSharedRect method, IRDPSRAPISharingSession2::GetDesktopSharedRect, IRDPSRAPISharingSession::GetDesktopSharedRect, rdp.irdpsrapisharingsession_getdesktopsharedrect, rdpencomapi/IRDPSRAPISharingSession2::GetDesktopSharedRect, rdpencomapi/IRDPSRAPISharingSession::GetDesktopSharedRect
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
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPISharingSession::GetDesktopSharedRect
 - rdpencomapi/IRDPSRAPISharingSession::GetDesktopSharedRect
dev_langs:
 - c++
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
---

# IRDPSRAPISharingSession::GetDesktopSharedRect


## -description

Retrieves the current desktop region being shared.

## -parameters

### -param pleft [out]

Type: <b>long*</b>

X-coordinate of the upper-left corner of the shared rectangle.

### -param ptop [out]

Type: <b>long*</b>

Y-coordinate of the upper-left corner of the shared rectangle.

### -param pright [out]

Type: <b>long*</b>

X-coordinate of the lower-right corner of the shared rectangle.

### -param pbottom [out]

Type: <b>long*</b>

Y-coordinate of the lower-right corner of the shared rectangle.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
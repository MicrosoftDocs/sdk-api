---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.SetDesktopSharedRect
title: IRDPSRAPISharingSession::SetDesktopSharedRect (rdpencomapi.h)
description: Sets the desktop region that will be shared.
helpviewer_keywords: ["IRDPSRAPISharingSession interface [RDP]","SetDesktopSharedRect method","IRDPSRAPISharingSession.SetDesktopSharedRect","IRDPSRAPISharingSession2 interface [RDP]","SetDesktopSharedRect method","IRDPSRAPISharingSession2::SetDesktopSharedRect","IRDPSRAPISharingSession::SetDesktopSharedRect","SetDesktopSharedRect","SetDesktopSharedRect method [RDP]","SetDesktopSharedRect method [RDP]","IRDPSRAPISharingSession interface","SetDesktopSharedRect method [RDP]","IRDPSRAPISharingSession2 interface","rdp.irdpsrapisharingsession_setdesktopsharedrect","rdpencomapi/IRDPSRAPISharingSession2::SetDesktopSharedRect","rdpencomapi/IRDPSRAPISharingSession::SetDesktopSharedRect"]
old-location: rdp\irdpsrapisharingsession_setdesktopsharedrect.htm
tech.root: rdp
ms.assetid: 8dda8b52-5bec-45ed-9215-2009cb74bf3e
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession interface [RDP],SetDesktopSharedRect method, IRDPSRAPISharingSession.SetDesktopSharedRect, IRDPSRAPISharingSession2 interface [RDP],SetDesktopSharedRect method, IRDPSRAPISharingSession2::SetDesktopSharedRect, IRDPSRAPISharingSession::SetDesktopSharedRect, SetDesktopSharedRect, SetDesktopSharedRect method [RDP], SetDesktopSharedRect method [RDP],IRDPSRAPISharingSession interface, SetDesktopSharedRect method [RDP],IRDPSRAPISharingSession2 interface, rdp.irdpsrapisharingsession_setdesktopsharedrect, rdpencomapi/IRDPSRAPISharingSession2::SetDesktopSharedRect, rdpencomapi/IRDPSRAPISharingSession::SetDesktopSharedRect
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
 - IRDPSRAPISharingSession::SetDesktopSharedRect
 - rdpencomapi/IRDPSRAPISharingSession::SetDesktopSharedRect
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
 - IRDPSRAPISharingSession2.SetDesktopSharedRect
 - IRDPSRAPISharingSession.SetDesktopSharedRect
---

# IRDPSRAPISharingSession::SetDesktopSharedRect


## -description

Sets the desktop region that will be shared.

## -parameters

### -param left [in]

Type: <b>long</b>

X-coordinate of the upper-left corner of the shared rectangle.

### -param top [in]

Type: <b>long</b>

Y-coordinate of the upper-left corner of the shared rectangle.

### -param right [in]

Type: <b>long</b>

X-coordinate of the lower-right corner of the shared rectangle.

### -param bottom [in]

Type: <b>long</b>

Y-coordinate of the lower-right corner of the shared rectangle.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
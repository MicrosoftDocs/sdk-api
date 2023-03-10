---
UID: NF:rdpencomapi.IRDPSRAPIViewer.RequestColorDepthChange
title: IRDPSRAPIViewer::RequestColorDepthChange (rdpencomapi.h)
description: Requests a color depth change on the sharer Winlogon user session.
helpviewer_keywords: ["IRDPSRAPIViewer interface [RDP]","RequestColorDepthChange method","IRDPSRAPIViewer.RequestColorDepthChange","IRDPSRAPIViewer::RequestColorDepthChange","RequestColorDepthChange","RequestColorDepthChange method [RDP]","RequestColorDepthChange method [RDP]","IRDPSRAPIViewer interface","rdp.irdpsrapiviewer_requestcolordepthchange","rdpencomapi/IRDPSRAPIViewer::RequestColorDepthChange"]
old-location: rdp\irdpsrapiviewer_requestcolordepthchange.htm
tech.root: rdp
ms.assetid: 3dd57235-89bb-4199-a95a-d8f522cda6a2
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIViewer interface [RDP],RequestColorDepthChange method, IRDPSRAPIViewer.RequestColorDepthChange, IRDPSRAPIViewer::RequestColorDepthChange, RequestColorDepthChange, RequestColorDepthChange method [RDP], RequestColorDepthChange method [RDP],IRDPSRAPIViewer interface, rdp.irdpsrapiviewer_requestcolordepthchange, rdpencomapi/IRDPSRAPIViewer::RequestColorDepthChange
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IRDPSRAPIViewer::RequestColorDepthChange
 - rdpencomapi/IRDPSRAPIViewer::RequestColorDepthChange
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
 - IRDPSRAPIViewer.RequestColorDepthChange
---

# IRDPSRAPIViewer::RequestColorDepthChange


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Requests a color depth change on the sharer Winlogon user session.

## -parameters

### -param Bpp [in]

Type: <b>long</b>

Specifies  the color depth of the session in bits per pixel.  Possible values are 16 and 24. If you specify a value of 8, the color depth is set to 16 bits per pixel.

<b>Windows Server 2008 and Windows Vista:  </b>Possible values are 8, 16, and 24.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a>
---
UID: NF:rdpencomapi.IRDPSRAPIViewer.put_DisconnectedText
title: IRDPSRAPIViewer::put_DisconnectedText (rdpencomapi.h)
description: Retrieves or sets the text that appears centered in the control before a connection is terminated. (Put)
helpviewer_keywords: ["DisconnectedText property [RDP]","DisconnectedText property [RDP]","IRDPSRAPIViewer interface","DisconnectedText property [RDP]","RDPViewer object","IRDPSRAPIViewer interface [RDP]","DisconnectedText property","IRDPSRAPIViewer.DisconnectedText","IRDPSRAPIViewer.put_DisconnectedText","IRDPSRAPIViewer::DisconnectedText","IRDPSRAPIViewer::get_DisconnectedText","IRDPSRAPIViewer::put_DisconnectedText","RDPViewer object [RDP]","DisconnectedText property","put_DisconnectedText","rdp.irdpsrapiviewer_disconnectedtext","rdpencomapi/IRDPSRAPIViewer::DisconnectedText","rdpencomapi/IRDPSRAPIViewer::get_DisconnectedText","rdpencomapi/IRDPSRAPIViewer::put_DisconnectedText"]
old-location: rdp\irdpsrapiviewer_disconnectedtext.htm
tech.root: rdp
ms.assetid: 010974ee-d5b0-436d-9553-18ae62d09bf2
ms.date: 12/05/2018
ms.keywords: DisconnectedText property [RDP], DisconnectedText property [RDP],IRDPSRAPIViewer interface, DisconnectedText property [RDP],RDPViewer object, IRDPSRAPIViewer interface [RDP],DisconnectedText property, IRDPSRAPIViewer.DisconnectedText, IRDPSRAPIViewer.put_DisconnectedText, IRDPSRAPIViewer::DisconnectedText, IRDPSRAPIViewer::get_DisconnectedText, IRDPSRAPIViewer::put_DisconnectedText, RDPViewer object [RDP],DisconnectedText property, put_DisconnectedText, rdp.irdpsrapiviewer_disconnectedtext, rdpencomapi/IRDPSRAPIViewer::DisconnectedText, rdpencomapi/IRDPSRAPIViewer::get_DisconnectedText, rdpencomapi/IRDPSRAPIViewer::put_DisconnectedText
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
 - IRDPSRAPIViewer::put_DisconnectedText
 - rdpencomapi/IRDPSRAPIViewer::put_DisconnectedText
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
 - IRDPSRAPIViewer.DisconnectedText
 - IRDPSRAPIViewer.get_DisconnectedText
 - IRDPSRAPIViewer.put_DisconnectedText
 - RDPViewer.DisconnectedText
---

# IRDPSRAPIViewer::put_DisconnectedText


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Retrieves or sets the text that appears centered in the control before a connection is terminated.

This property is read/write.

## -parameters

## -remarks

Setting <b>DisconnectedText</b> is optional. If it is not specified, the control appears blank before a connection is established.

The <b>DisconnectedText</b> property can be set only if the control is not in the connected state. The method returns <b>E_FAIL</b> if it is called after the control is connected.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a>

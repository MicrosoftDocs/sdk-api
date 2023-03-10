---
UID: NS:pnrpns._PNRPCLOUDINFO
title: PNRPCLOUDINFO (pnrpns.h)
description: The PNRPCLOUDINFO structure is pointed to by the lpBlob member of the WSAQUERYSET structure.
helpviewer_keywords: ["*PPNRPCLOUDINFO","PNRPCLOUDINFO","PNRPCLOUDINFO structure [Peer Networking]","PPNRPCLOUDINFO","PPNRPCLOUDINFO structure pointer [Peer Networking]","p2p.pnrpcloudinfo","pnrpns/PNRPCLOUDINFO","pnrpns/PPNRPCLOUDINFO"]
old-location: p2p\pnrpcloudinfo.htm
tech.root: p2p
ms.assetid: 82af5a4f-1b29-405a-a200-1d723ea7693b
ms.date: 12/05/2018
ms.keywords: '*PPNRPCLOUDINFO, PNRPCLOUDINFO, PNRPCLOUDINFO structure [Peer Networking], PPNRPCLOUDINFO, PPNRPCLOUDINFO structure pointer [Peer Networking], p2p.pnrpcloudinfo, pnrpns/PNRPCLOUDINFO, pnrpns/PPNRPCLOUDINFO'
req.header: pnrpns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PNRPCLOUDINFO, *PPNRPCLOUDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PNRPCLOUDINFO
 - pnrpns/_PNRPCLOUDINFO
 - PPNRPCLOUDINFO
 - pnrpns/PPNRPCLOUDINFO
 - PNRPCLOUDINFO
 - pnrpns/PNRPCLOUDINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pnrpns.h
api_name:
 - PNRPCLOUDINFO
---

# PNRPCLOUDINFO structure


## -description

The <b>PNRPCLOUDINFO</b> structure is pointed to by the <b>lpBlob</b> member of the <a href="/windows/desktop/P2PSdk/winsock-nsp-reference-links">WSAQUERYSET</a> structure.

## -struct-fields

### -field dwSize

Specifies the size of this structure.

### -field Cloud

Specifies the network cloud information stored in a <a href="/windows/desktop/api/pnrpdef/ns-pnrpdef-pnrp_cloud_id">PNRP_CLOUD_ID</a> structure.

### -field enCloudState

Specifies the state of the network cloud. Valid values are specified by <a href="/windows/desktop/api/pnrpdef/ne-pnrpdef-pnrp_cloud_state">PNRP_CLOUD_STATE</a>.

### -field enCloudFlags

Indicates if the cloud name is valid on the network or only valid on the current computer. Valid values are specified by <a href="/windows/desktop/api/pnrpdef/ne-pnrpdef-pnrp_cloud_flags">PNRP_CLOUD_FLAGS</a>.

## -see-also

<a href="/windows/desktop/P2PSdk/pnrp-and-blob">PNRP and BLOB</a>



<a href="/windows/desktop/P2PSdk/pnrp-and-wsalookupservicebegin">PNRP and WSALookupServiceBegin</a>



<a href="/windows/desktop/P2PSdk/pnrp-and-wsalookupservicenext">PNRP and WSALookupServiceNext</a>



<a href="/windows/desktop/P2PSdk/pnrp-and-wsaqueryset">PNRP and WSAQUERYSET</a>



<a href="/windows/desktop/api/pnrpdef/ne-pnrpdef-pnrp_cloud_flags">PNRP_CLOUD_FLAGS</a>



<a href="/windows/desktop/api/pnrpdef/ns-pnrpdef-pnrp_cloud_id">PNRP_CLOUD_ID</a>



<a href="/windows/desktop/api/pnrpdef/ne-pnrpdef-pnrp_cloud_state">PNRP_CLOUD_STATE</a>



<a href="/windows/desktop/P2PSdk/winsock-nsp-reference-links">WSAQUERYSET</a>
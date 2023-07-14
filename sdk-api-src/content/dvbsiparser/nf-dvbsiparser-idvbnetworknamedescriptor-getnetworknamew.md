---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetNetworkNameW
title: IDvbNetworkNameDescriptor::GetNetworkNameW (dvbsiparser.h)
description: Gets the network name, in Unicode string format, from a Digital Video Broadcast (DVB) network name descriptor.
helpviewer_keywords: ["GetNetworkNameW","GetNetworkNameW method [Microsoft TV Technologies]","GetNetworkNameW method [Microsoft TV Technologies]","IDvbNetworkNameDescriptor interface","IDvbNetworkNameDescriptor interface [Microsoft TV Technologies]","GetNetworkNameW method","IDvbNetworkNameDescriptor.GetNetworkNameW","IDvbNetworkNameDescriptor::GetNetworkNameW","dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkNameW","mstv.idvbnetworknamedescriptor_getnetworknamew"]
old-location: mstv\idvbnetworknamedescriptor_getnetworknamew.htm
tech.root: mstv
ms.assetid: 2c7e1507-2b55-468d-b83d-643a45118429
ms.date: 12/05/2018
ms.keywords: GetNetworkNameW, GetNetworkNameW method [Microsoft TV Technologies], GetNetworkNameW method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetNetworkNameW method, IDvbNetworkNameDescriptor.GetNetworkNameW, IDvbNetworkNameDescriptor::GetNetworkNameW, dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkNameW, mstv.idvbnetworknamedescriptor_getnetworknamew
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbNetworkNameDescriptor::GetNetworkNameW
 - dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbNetworkNameDescriptor.GetNetworkNameW
---

# IDvbNetworkNameDescriptor::GetNetworkNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the network name, in Unicode string format, from a Digital Video Broadcast (DVB) network name descriptor.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrName [out]

Pointer to a string buffer that receives the network name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbnetworknamedescriptor">IDvbNetworkNameDescriptor</a>
---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetPrivateData
title: IDvbLinkageDescriptor::GetPrivateData (dvbsiparser.h)
description: Gets the private data from a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetPrivateData","GetPrivateData method [Microsoft TV Technologies]","GetPrivateData method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetPrivateData method","IDvbLinkageDescriptor.GetPrivateData","IDvbLinkageDescriptor::GetPrivateData","dvbsiparser/IDvbLinkageDescriptor::GetPrivateData","mstv.idvblinkagedescriptor_getprivatedata"]
old-location: mstv\idvblinkagedescriptor_getprivatedata.htm
tech.root: mstv
ms.assetid: 959aeb87-b661-4567-a6fd-2d28be6b0a02
ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method [Microsoft TV Technologies], GetPrivateData method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetPrivateData method, IDvbLinkageDescriptor.GetPrivateData, IDvbLinkageDescriptor::GetPrivateData, dvbsiparser/IDvbLinkageDescriptor::GetPrivateData, mstv.idvblinkagedescriptor_getprivatedata
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDvbLinkageDescriptor::GetPrivateData
 - dvbsiparser/IDvbLinkageDescriptor::GetPrivateData
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
 - IDvbLinkageDescriptor.GetPrivateData
---

# IDvbLinkageDescriptor::GetPrivateData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the private data from a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pbLen [in, out]

On input, specifies the size of the buffer (pointed to by the <i>pbData</i> parameter) allocated for the private data, in bytes. On output, gets the actual length of the private  data that is received.

### -param pbData [out]

Receives private data from the DVB linkage descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>
---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListCountryCode
title: IDvbLogicalChannel2Descriptor::GetListCountryCode (dvbsiparser.h)
description: Gets the three-character ISO 3166 country code for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.
helpviewer_keywords: ["GetListCountryCode","GetListCountryCode method [Microsoft TV Technologies]","GetListCountryCode method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetListCountryCode method","IDvbLogicalChannel2Descriptor.GetListCountryCode","IDvbLogicalChannel2Descriptor::GetListCountryCode","dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountryCode","mstv.idvblogicalchannel2descriptor_getlistcountrycode"]
old-location: mstv\idvblogicalchannel2descriptor_getlistcountrycode.htm
tech.root: mstv
ms.assetid: 42f3c684-64c3-4bcb-b9c0-25a008075902
ms.date: 12/05/2018
ms.keywords: GetListCountryCode, GetListCountryCode method [Microsoft TV Technologies], GetListCountryCode method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListCountryCode method, IDvbLogicalChannel2Descriptor.GetListCountryCode, IDvbLogicalChannel2Descriptor::GetListCountryCode, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountryCode, mstv.idvblogicalchannel2descriptor_getlistcountrycode
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
 - IDvbLogicalChannel2Descriptor::GetListCountryCode
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountryCode
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
 - IDvbLogicalChannel2Descriptor.GetListCountryCode
---

# IDvbLogicalChannel2Descriptor::GetListCountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 3166 country code for a channel list in a  Digital Video Broadcast (DVB) logical channel descriptor.

## -parameters

### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a> method to get the number of channel list records in the logical channel descriptor.

### -param pszCode [out]

Pointer to a buffer that receives the country code. This code is a 3-character, null-terminated string, so the buffer must be at least four bytes long. The caller is responsible for releasing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>
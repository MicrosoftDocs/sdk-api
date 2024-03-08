---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListNameW
title: IDvbLogicalChannel2Descriptor::GetListNameW (dvbsiparser.h)
description: Gets the name of a channel list from a Digital Video Broadcast (DVB) logical channel descriptor.
helpviewer_keywords: ["GetListNameW","GetListNameW method [Microsoft TV Technologies]","GetListNameW method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetListNameW method","IDvbLogicalChannel2Descriptor.GetListNameW","IDvbLogicalChannel2Descriptor::GetListNameW","dvbsiparser/IDvbLogicalChannel2Descriptor::GetListNameW","mstv.idvblogicalchannel2descriptor_getlistnamew"]
old-location: mstv\idvblogicalchannel2descriptor_getlistnamew.htm
tech.root: mstv
ms.assetid: cbfee1d5-8a38-4c9a-ae5e-2d91970c132e
ms.date: 12/05/2018
ms.keywords: GetListNameW, GetListNameW method [Microsoft TV Technologies], GetListNameW method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListNameW method, IDvbLogicalChannel2Descriptor.GetListNameW, IDvbLogicalChannel2Descriptor::GetListNameW, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListNameW, mstv.idvblogicalchannel2descriptor_getlistnamew
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
 - IDvbLogicalChannel2Descriptor::GetListNameW
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetListNameW
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
 - IDvbLogicalChannel2Descriptor.GetListNameW
---

# IDvbLogicalChannel2Descriptor::GetListNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the name of a channel list from a Digital Video Broadcast (DVB) logical channel descriptor.

## -parameters

### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a> method to get the number of channel list records in the logical channel descriptor.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrName [out]

Pointer to the memory block that receives the channel name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
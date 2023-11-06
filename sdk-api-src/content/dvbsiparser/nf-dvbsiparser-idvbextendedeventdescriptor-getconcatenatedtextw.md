---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetConcatenatedTextW
title: IDvbExtendedEventDescriptor::GetConcatenatedTextW (dvbsiparser.h)
description: Gets the concatenation of the text description in the current item with the text description in the next item (both in Unicode format) of a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetConcatenatedTextW","GetConcatenatedTextW method [Microsoft TV Technologies]","GetConcatenatedTextW method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetConcatenatedTextW method","IDvbExtendedEventDescriptor.GetConcatenatedTextW","IDvbExtendedEventDescriptor::GetConcatenatedTextW","dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedTextW","mstv.idvbextendedeventdescriptor_getconcatenatedtextw"]
old-location: mstv\idvbextendedeventdescriptor_getconcatenatedtextw.htm
tech.root: mstv
ms.assetid: d8cbfe2c-db33-449d-991c-5fb50d8d974f
ms.date: 12/05/2018
ms.keywords: GetConcatenatedTextW, GetConcatenatedTextW method [Microsoft TV Technologies], GetConcatenatedTextW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetConcatenatedTextW method, IDvbExtendedEventDescriptor.GetConcatenatedTextW, IDvbExtendedEventDescriptor::GetConcatenatedTextW, dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedTextW, mstv.idvbextendedeventdescriptor_getconcatenatedtextw
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
 - IDvbExtendedEventDescriptor::GetConcatenatedTextW
 - dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedTextW
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
 - IDvbExtendedEventDescriptor.GetConcatenatedTextW
---

# IDvbExtendedEventDescriptor::GetConcatenatedTextW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the concatenation of the text description in the current item with the text description in the next item (both in Unicode format) of a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param FollowingDescriptor [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a> interface for the next extended event descriptor that is associated with the current event descriptor.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrText [out]

Pointer to the buffer that receives the concatenated item text. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>
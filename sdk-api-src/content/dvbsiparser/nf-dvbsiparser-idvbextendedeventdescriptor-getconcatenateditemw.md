---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetConcatenatedItemW
title: IDvbExtendedEventDescriptor::GetConcatenatedItemW (dvbsiparser.h)
description: Concatenates the bytes from the item in the current Digital Video Broadcast (DVB) extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.
helpviewer_keywords: ["GetConcatenatedItemW","GetConcatenatedItemW method [Microsoft TV Technologies]","GetConcatenatedItemW method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetConcatenatedItemW method","IDvbExtendedEventDescriptor.GetConcatenatedItemW","IDvbExtendedEventDescriptor::GetConcatenatedItemW","dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedItemW","mstv.idvbextendedeventdescriptor_getconcatenateditemw"]
old-location: mstv\idvbextendedeventdescriptor_getconcatenateditemw.htm
tech.root: mstv
ms.assetid: 9b90a2de-8447-4038-9a11-1db74ebd2feb
ms.date: 12/05/2018
ms.keywords: GetConcatenatedItemW, GetConcatenatedItemW method [Microsoft TV Technologies], GetConcatenatedItemW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetConcatenatedItemW method, IDvbExtendedEventDescriptor.GetConcatenatedItemW, IDvbExtendedEventDescriptor::GetConcatenatedItemW, dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedItemW, mstv.idvbextendedeventdescriptor_getconcatenateditemw
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
 - IDvbExtendedEventDescriptor::GetConcatenatedItemW
 - dvbsiparser/IDvbExtendedEventDescriptor::GetConcatenatedItemW
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
 - IDvbExtendedEventDescriptor.GetConcatenatedItemW
---

# IDvbExtendedEventDescriptor::GetConcatenatedItemW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Concatenates the bytes from the item in the current Digital Video Broadcast (DVB) extended event descriptor with the bytes from the item in the next DVB extended event descriptor and returns the concatenated data as a Unicode string.

## -parameters

### -param pFollowingDescriptor [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a> interface for the next DVB extended event descriptor associated with the current one.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrDesc [out]

Pointer to a buffer that receives the concatenated item descriptor. The caller is responsible for freeing this memory.

### -param pbstrItem [out]

Pointer to a buffer that receives the concatenated item string. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>
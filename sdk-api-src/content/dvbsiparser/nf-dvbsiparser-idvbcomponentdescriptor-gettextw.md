---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetTextW
title: IDvbComponentDescriptor::GetTextW (dvbsiparser.h)
description: Gets the text describing the elementary stream, in Unicode string format, from a Digital Video Broadcast (DVB) component descriptor.
helpviewer_keywords: ["GetTextW","GetTextW method [Microsoft TV Technologies]","GetTextW method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetTextW method","IDvbComponentDescriptor.GetTextW","IDvbComponentDescriptor::GetTextW","dvbsiparser/IDvbComponentDescriptor::GetTextW","mstv.idvbcomponentdescriptor_gettextw"]
old-location: mstv\idvbcomponentdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: 1b4ff757-24d0-4dca-8def-c8079724e571
ms.date: 12/05/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetTextW method, IDvbComponentDescriptor.GetTextW, IDvbComponentDescriptor::GetTextW, dvbsiparser/IDvbComponentDescriptor::GetTextW, mstv.idvbcomponentdescriptor_gettextw
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
 - IDvbComponentDescriptor::GetTextW
 - dvbsiparser/IDvbComponentDescriptor::GetTextW
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
 - IDvbComponentDescriptor.GetTextW
---

# IDvbComponentDescriptor::GetTextW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the text describing the elementary stream, in Unicode string format, from a Digital Video Broadcast (DVB) component descriptor.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrText [out]

Receives the event description text. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>
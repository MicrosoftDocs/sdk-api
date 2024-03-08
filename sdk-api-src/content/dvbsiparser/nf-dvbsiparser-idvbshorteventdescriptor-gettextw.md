---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetTextW
title: IDvbShortEventDescriptor::GetTextW (dvbsiparser.h)
description: Gets the text that describes the event in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.
helpviewer_keywords: ["GetTextW","GetTextW method [Microsoft TV Technologies]","GetTextW method [Microsoft TV Technologies]","IDvbShortEventDescriptor interface","IDvbShortEventDescriptor interface [Microsoft TV Technologies]","GetTextW method","IDvbShortEventDescriptor.GetTextW","IDvbShortEventDescriptor::GetTextW","dvbsiparser/IDvbShortEventDescriptor::GetTextW","mstv.idvbshorteventdescriptor_gettextw"]
old-location: mstv\idvbshorteventdescriptor_gettextw.htm
tech.root: mstv
ms.assetid: 0770d24f-b421-4b00-809c-04fa53ca038c
ms.date: 12/05/2018
ms.keywords: GetTextW, GetTextW method [Microsoft TV Technologies], GetTextW method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetTextW method, IDvbShortEventDescriptor.GetTextW, IDvbShortEventDescriptor::GetTextW, dvbsiparser/IDvbShortEventDescriptor::GetTextW, mstv.idvbshorteventdescriptor_gettextw
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
 - IDvbShortEventDescriptor::GetTextW
 - dvbsiparser/IDvbShortEventDescriptor::GetTextW
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
 - IDvbShortEventDescriptor.GetTextW
---

# IDvbShortEventDescriptor::GetTextW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the text that describes the event in Unicode string format from a Digital Video Broadcast (DVB) short event descriptor.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrText [out]

Pointer to a buffer that receives the event description text. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbshorteventdescriptor">IDvbShortEventDescriptor</a>
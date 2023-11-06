---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetStreamType
title: IIsdbAudioComponentDescriptor::GetStreamType (dvbsiparser.h)
description: Gets a code that indicates the stream type from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
helpviewer_keywords: ["GetStreamType","GetStreamType method [Microsoft TV Technologies]","GetStreamType method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetStreamType method","IIsdbAudioComponentDescriptor.GetStreamType","IIsdbAudioComponentDescriptor::GetStreamType","dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamType","mstv.iisdbaudiocomponentdescriptor_getstreamtype"]
old-location: mstv\iisdbaudiocomponentdescriptor_getstreamtype.htm
tech.root: mstv
ms.assetid: 73c7a8c8-7098-43e8-ac90-c29586e9856c
ms.date: 12/05/2018
ms.keywords: GetStreamType, GetStreamType method [Microsoft TV Technologies], GetStreamType method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetStreamType method, IIsdbAudioComponentDescriptor.GetStreamType, IIsdbAudioComponentDescriptor::GetStreamType, dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamType, mstv.iisdbaudiocomponentdescriptor_getstreamtype
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
 - IIsdbAudioComponentDescriptor::GetStreamType
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamType
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
 - IIsdbAudioComponentDescriptor.GetStreamType
---

# IIsdbAudioComponentDescriptor::GetStreamType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a code that indicates the stream type from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. See Annex E, Table E-4 <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM
ARIB STANDARD,
ARIB STD-B10, Version 4.6</i> for a list of valid stream type codes.

.

## -parameters

### -param pbVal [out]

Receives the stream type code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetTag
title: IIsdbAudioComponentDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbAudioComponentDescriptor.GetTag","IIsdbAudioComponentDescriptor::GetTag","dvbsiparser/IIsdbAudioComponentDescriptor::GetTag","mstv.iisdbaudiocomponentdescriptor_gettag"]
old-location: mstv\iisdbaudiocomponentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: b44ef442-3bfc-4b1f-b64d-4be21fc1fb47
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbAudioComponentDescriptor.GetTag, IIsdbAudioComponentDescriptor::GetTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetTag, mstv.iisdbaudiocomponentdescriptor_gettag
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
 - IIsdbAudioComponentDescriptor::GetTag
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetTag
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
 - IIsdbAudioComponentDescriptor.GetTag
---

# IIsdbAudioComponentDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For ISDB audio component descriptors, this value is 0xC4.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
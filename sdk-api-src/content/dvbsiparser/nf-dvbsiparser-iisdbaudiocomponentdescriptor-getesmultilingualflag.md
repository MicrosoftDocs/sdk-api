---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetESMultiLingualFlag
title: IIsdbAudioComponentDescriptor::GetESMultiLingualFlag (dvbsiparser.h)
description: Gets a flag from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the stream uses ES multilingual mode.
helpviewer_keywords: ["GetESMultiLingualFlag","GetESMultiLingualFlag method [Microsoft TV Technologies]","GetESMultiLingualFlag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetESMultiLingualFlag method","IIsdbAudioComponentDescriptor.GetESMultiLingualFlag","IIsdbAudioComponentDescriptor::GetESMultiLingualFlag","dvbsiparser/IIsdbAudioComponentDescriptor::GetESMultiLingualFlag","mstv.iisdbaudiocomponentdescriptor_getesmultilingualflag"]
old-location: mstv\iisdbaudiocomponentdescriptor_getesmultilingualflag.htm
tech.root: mstv
ms.assetid: 10a47ca7-84db-48de-8ba5-0be257438044
ms.date: 12/05/2018
ms.keywords: GetESMultiLingualFlag, GetESMultiLingualFlag method [Microsoft TV Technologies], GetESMultiLingualFlag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetESMultiLingualFlag method, IIsdbAudioComponentDescriptor.GetESMultiLingualFlag, IIsdbAudioComponentDescriptor::GetESMultiLingualFlag, dvbsiparser/IIsdbAudioComponentDescriptor::GetESMultiLingualFlag, mstv.iisdbaudiocomponentdescriptor_getesmultilingualflag
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
 - IIsdbAudioComponentDescriptor::GetESMultiLingualFlag
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetESMultiLingualFlag
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
 - IIsdbAudioComponentDescriptor.GetESMultiLingualFlag
---

# IIsdbAudioComponentDescriptor::GetESMultiLingualFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a flag  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the stream uses ES multilingual mode.

## -parameters

### -param pfVal [out]

Receives 1 if the stream uses ES multilingual mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

ES multilingual mode (also called <i>2-language multilingual mode</i> or <i>1/0  + 1/0 mode</i>) is a dual-channel monaural mode indicated by a value of 0x02 in the component_type field of the descriptor.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
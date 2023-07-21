---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetMainComponentFlag
title: IIsdbAudioComponentDescriptor::GetMainComponentFlag (dvbsiparser.h)
description: Gets a flag from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the audio component is the main audio.
helpviewer_keywords: ["GetMainComponentFlag","GetMainComponentFlag method [Microsoft TV Technologies]","GetMainComponentFlag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetMainComponentFlag method","IIsdbAudioComponentDescriptor.GetMainComponentFlag","IIsdbAudioComponentDescriptor::GetMainComponentFlag","dvbsiparser/IIsdbAudioComponentDescriptor::GetMainComponentFlag","mstv.iisdbaudiocomponentdescriptor_getmaincomponentflag"]
old-location: mstv\iisdbaudiocomponentdescriptor_getmaincomponentflag.htm
tech.root: mstv
ms.assetid: 223bb5d2-2b19-44e7-a347-16b2930f00a6
ms.date: 12/05/2018
ms.keywords: GetMainComponentFlag, GetMainComponentFlag method [Microsoft TV Technologies], GetMainComponentFlag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetMainComponentFlag method, IIsdbAudioComponentDescriptor.GetMainComponentFlag, IIsdbAudioComponentDescriptor::GetMainComponentFlag, dvbsiparser/IIsdbAudioComponentDescriptor::GetMainComponentFlag, mstv.iisdbaudiocomponentdescriptor_getmaincomponentflag
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
 - IIsdbAudioComponentDescriptor::GetMainComponentFlag
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetMainComponentFlag
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
 - IIsdbAudioComponentDescriptor.GetMainComponentFlag
---

# IIsdbAudioComponentDescriptor::GetMainComponentFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a flag  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the audio component is the main audio.

## -parameters

### -param pfVal [out]

Receives 1 if the audio component is the main audio or 0 if it is not. In ES simulcast mode, receives 1 if the first audio component is the main audio or 0 if it is not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
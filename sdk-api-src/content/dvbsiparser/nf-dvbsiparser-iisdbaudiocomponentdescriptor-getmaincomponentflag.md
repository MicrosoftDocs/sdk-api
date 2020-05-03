---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetMainComponentFlag
title: IIsdbAudioComponentDescriptor::GetMainComponentFlag (dvbsiparser.h)
description: Gets a flag from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the audio component is the main audio.helpviewer_keywords: ["GetMainComponentFlag","GetMainComponentFlag method [Microsoft TV Technologies]","GetMainComponentFlag method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetMainComponentFlag method","IIsdbAudioComponentDescriptor.GetMainComponentFlag","IIsdbAudioComponentDescriptor::GetMainComponentFlag","dvbsiparser/IIsdbAudioComponentDescriptor::GetMainComponentFlag","mstv.iisdbaudiocomponentdescriptor_getmaincomponentflag"]
old-location: mstv\iisdbaudiocomponentdescriptor_getmaincomponentflag.htm
tech.root: mstv
ms.assetid: 223bb5d2-2b19-44e7-a347-16b2930f00a6
ms.date: 12/05/2018
ms.keywords: GetMainComponentFlag, GetMainComponentFlag method [Microsoft TV Technologies], GetMainComponentFlag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetMainComponentFlag method, IIsdbAudioComponentDescriptor.GetMainComponentFlag, IIsdbAudioComponentDescriptor::GetMainComponentFlag, dvbsiparser/IIsdbAudioComponentDescriptor::GetMainComponentFlag, mstv.iisdbaudiocomponentdescriptor_getmaincomponentflag
f1_keywords:
- dvbsiparser/IIsdbAudioComponentDescriptor.GetMainComponentFlag
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbAudioComponentDescriptor.GetMainComponentFlag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetMainComponentFlag


## -description


Gets a flag  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the audio component is the main audio. 


## -parameters




### -param pfVal [out]

Receives 1 if the audio component is the main audio or 0 if it is not. In ES simulcast mode, receives 1 if the first audio component is the main audio or 0 if it is not.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 


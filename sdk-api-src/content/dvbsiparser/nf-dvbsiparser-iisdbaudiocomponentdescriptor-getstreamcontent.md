---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetStreamContent
title: IIsdbAudioComponentDescriptor::GetStreamContent (dvbsiparser.h)
author: windows-sdk-content
description: Gets the value of the stream_content field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field contains a code that identifies the descriptor as an ISDB audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor_getstreamcontent.htm
tech.root: mstv
ms.assetid: 1283c029-d1f5-4da8-a0fe-c795b4cd093c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStreamContent, GetStreamContent method [Microsoft TV Technologies], GetStreamContent method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetStreamContent method, IIsdbAudioComponentDescriptor.GetStreamContent, IIsdbAudioComponentDescriptor::GetStreamContent, dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamContent, mstv.iisdbaudiocomponentdescriptor_getstreamcontent
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbAudioComponentDescriptor.GetStreamContent"
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
 - IIsdbAudioComponentDescriptor.GetStreamContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetStreamContent


## -description


Gets the value of the stream_content field  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field contains a code that identifies the descriptor as an ISDB audio component descriptor.


## -parameters




### -param pbVal [out]

Receives the stream_content field value. For audio streams, this value is 0x02.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 


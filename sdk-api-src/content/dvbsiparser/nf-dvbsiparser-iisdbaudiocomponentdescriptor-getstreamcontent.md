---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetStreamContent
title: IIsdbAudioComponentDescriptor::GetStreamContent method
author: windows-driver-content
description: Gets the value of the stream_content field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field contains a code that identifies the descriptor as an ISDB audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor_getstreamcontent.htm
old-project: mstv
ms.assetid: 1283c029-d1f5-4da8-a0fe-c795b4cd093c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetStreamContent method [Microsoft TV Technologies], GetStreamContent method [Microsoft TV Technologies], IIsdbAudioComponentDescriptor interface, GetStreamContent,IIsdbAudioComponentDescriptor.GetStreamContent, IIsdbAudioComponentDescriptor, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies], GetStreamContent method, IIsdbAudioComponentDescriptor::GetStreamContent, dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamContent, mstv.iisdbaudiocomponentdescriptor_getstreamcontent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbAudioComponentDescriptor.GetStreamContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor::GetStreamContent method


## -description


Gets the value of the stream_content field  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field contains a code that identifies the descriptor as an ISDB audio component descriptor.


## -parameters




### -param pbVal [out]

Receives the stream_content field value. For audio streams, this value is 0x02.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 


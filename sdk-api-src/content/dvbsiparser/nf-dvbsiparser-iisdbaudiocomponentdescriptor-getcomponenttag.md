---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetComponentTag
title: IIsdbAudioComponentDescriptor::GetComponentTag
author: windows-sdk-content
description: Gets the value of the component_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor_getcomponenttag.htm
tech.root: mstv
ms.assetid: 4b06f566-b5e0-43c8-8694-24d913bbf971
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetComponentTag, GetComponentTag method [Microsoft TV Technologies], GetComponentTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetComponentTag method, IIsdbAudioComponentDescriptor.GetComponentTag, IIsdbAudioComponentDescriptor::GetComponentTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetComponentTag, mstv.iisdbaudiocomponentdescriptor_getcomponenttag
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
 - IIsdbAudioComponentDescriptor.GetComponentTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbAudioComponentDescriptor::GetComponentTag


## -description


 Gets the value of the component_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field identifies the component stream and has the same value
as the component_tag field in the stream identifier descriptor in
the Program Specific Information (PSI) program map section for the component stream.


## -parameters




### -param pbVal [out]

Receives the component tag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 


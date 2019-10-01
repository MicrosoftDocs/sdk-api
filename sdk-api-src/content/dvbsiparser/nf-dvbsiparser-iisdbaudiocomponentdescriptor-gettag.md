---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetTag
title: IIsdbAudioComponentDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: b44ef442-3bfc-4b1f-b64d-4be21fc1fb47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbAudioComponentDescriptor.GetTag, IIsdbAudioComponentDescriptor::GetTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetTag, mstv.iisdbaudiocomponentdescriptor_gettag
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbAudioComponentDescriptor.GetTag"
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
 - IIsdbAudioComponentDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB audio component descriptors, this value is 0xC4.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 


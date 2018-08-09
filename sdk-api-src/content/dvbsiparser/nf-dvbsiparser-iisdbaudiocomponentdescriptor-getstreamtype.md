---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetStreamType
title: IIsdbAudioComponentDescriptor::GetStreamType
author: windows-sdk-content
description: Gets a code that indicates the stream type from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor_getstreamtype.htm
old-project: mstv
ms.assetid: 73c7a8c8-7098-43e8-ac90-c29586e9856c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetStreamType, GetStreamType method [Microsoft TV Technologies], GetStreamType method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetStreamType method, IIsdbAudioComponentDescriptor.GetStreamType, IIsdbAudioComponentDescriptor::GetStreamType, dvbsiparser/IIsdbAudioComponentDescriptor::GetStreamType, mstv.iisdbaudiocomponentdescriptor_getstreamtype
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbAudioComponentDescriptor.GetStreamType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor::GetStreamType


## -description


Gets a code that indicates the stream type from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. See Annex E, Table E-4 <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM
ARIB STANDARD,
ARIB STD-B10, Version 4.6</i> for a list of valid stream type codes.

.


## -parameters




### -param pbVal [out]

Receives the stream type code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 


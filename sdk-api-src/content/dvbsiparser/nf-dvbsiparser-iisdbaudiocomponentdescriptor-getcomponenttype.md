---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetComponentType
title: IIsdbAudioComponentDescriptor::GetComponentType
author: windows-sdk-content
description: Gets the value of the component_type field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field identifies the audio component type.
old-location: mstv\iisdbaudiocomponentdescriptor_getcomponenttype.htm
tech.root: MSTV
ms.assetid: 417deb6e-863e-4d62-8d58-685972f96f0c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetComponentType, GetComponentType method [Microsoft TV Technologies], GetComponentType method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetComponentType method, IIsdbAudioComponentDescriptor.GetComponentType, IIsdbAudioComponentDescriptor::GetComponentType, dvbsiparser/IIsdbAudioComponentDescriptor::GetComponentType, mstv.iisdbaudiocomponentdescriptor_getcomponenttype
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
 - IIsdbAudioComponentDescriptor.GetComponentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbAudioComponentDescriptor::GetComponentType


## -description


Gets the value of the component_type field  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field identifies the audio component type.


## -parameters




### -param pbVal [out]

Receives the component_type field value. See Table 6-43 in Section 6.2.26,  <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM
ARIB STANDARD,
ARIB STD-B10, Version 4.6</i> for a list of valid component type codes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 


---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetComponentType
title: IIsdbAudioComponentDescriptor::GetComponentType method
author: windows-driver-content
description: Gets the value of the component_type field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This field identifies the audio component type.
old-location: mstv\iisdbaudiocomponentdescriptor_getcomponenttype.htm
old-project: mstv
ms.assetid: 417deb6e-863e-4d62-8d58-685972f96f0c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetComponentType method [Microsoft TV Technologies], GetComponentType method [Microsoft TV Technologies], IIsdbAudioComponentDescriptor interface, GetComponentType,IIsdbAudioComponentDescriptor.GetComponentType, IIsdbAudioComponentDescriptor, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies], GetComponentType method, IIsdbAudioComponentDescriptor::GetComponentType, dvbsiparser/IIsdbAudioComponentDescriptor::GetComponentType, mstv.iisdbaudiocomponentdescriptor_getcomponenttype
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
-	IIsdbAudioComponentDescriptor.GetComponentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor::GetComponentType method


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
 

 


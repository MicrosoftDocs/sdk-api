---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetSimulcastGroupTag
title: IIsdbAudioComponentDescriptor::GetSimulcastGroupTag
author: windows-driver-content
description: Gets the value of the simulcast_group_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. For simulcast components, this field contains the tag that identifies all simulcast components.
old-location: mstv\iisdbaudiocomponentdescriptor_getsimulcastgrouptag.htm
old-project: mstv
ms.assetid: 125fa9c2-eba0-497b-82ca-cc3223e40b44
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetSimulcastGroupTag, GetSimulcastGroupTag method [Microsoft TV Technologies], GetSimulcastGroupTag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetSimulcastGroupTag method, IIsdbAudioComponentDescriptor.GetSimulcastGroupTag, IIsdbAudioComponentDescriptor::GetSimulcastGroupTag, dvbsiparser/IIsdbAudioComponentDescriptor::GetSimulcastGroupTag, mstv.iisdbaudiocomponentdescriptor_getsimulcastgrouptag
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
-	IIsdbAudioComponentDescriptor.GetSimulcastGroupTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor::GetSimulcastGroupTag


## -description


Gets the value of the simulcast_group_tag field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. For simulcast components, this field contains the tag that identifies all simulcast components. 


## -parameters




### -param pbVal [out]

Receives the simulcast group tag. For non-simulcast component, receives 0xFF.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 


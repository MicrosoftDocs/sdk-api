---
UID: NS:windows.media.streaming.TransportInformation
title: TransportInformation
author: windows-sdk-content
description: Contains the current values of media playback transport-related information obtained from the DMR.
old-location: mediastreaming\transportinformation.htm
tech.root: mediastreaming
ms.assetid: c91f84f2-e19b-4bfa-862d-fc5e1dc756d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TransportInformation, TransportInformation structure [Media Streaming API], mediastreaming.transportinformation, windows/TransportInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)
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
 - HeaderDef
api_location:
 - windows.media.streaming.h
api_name:
 - TransportInformation
product: Windows
targetos: Windows
req.typenames: TransportInformation
req.redist: 
---

# TransportInformation structure


## -description


Contains the current values of media playback transport-related information obtained from the DMR.


## -struct-fields




### -field streaming.TransportInformation.CurrentTransportState

 


### -field streaming.TransportInformation.CurrentTransportStatus

 


### -field streaming.TransportInformation.CurrentSpeed

 




#### - CurrentSpeed

A <a href="https://msdn.microsoft.com/29b58229-8236-4c93-a6b4-ed09d1aca9db">PlaySpeed</a> structure, indicating the current speed at which the DMR is playing the content, or was last playing the content.


#### - CurrentTransportState

A value from the <a href="https://msdn.microsoft.com/2F942EAC-514B-4E65-A12F-85558E9A96A0">TransportState</a> enumeration, indicating the current transport state of the DMR.


#### - CurrentTransportStatus

A value from the <a href="https://msdn.microsoft.com/6fde82f0-9bc4-4abb-9d10-0000501c2b24">TransportStatus</a> enumeration, indicating the current transport status reported by the DMR.


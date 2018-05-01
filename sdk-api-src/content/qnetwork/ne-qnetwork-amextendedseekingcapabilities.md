---
UID: NE:qnetwork.AMExtendedSeekingCapabilities
title: AMExtendedSeekingCapabilities
author: windows-driver-content
description: The AMExtendedSeekingCapabilities enumeration contains flags that describe the extended seeking capabilities of a filter.
old-location: dshow\amextendedseekingcapabilities.htm
old-project: DirectShow
ms.assetid: f5f21303-3b5b-45e8-a4dc-6c8bc7cd8ad3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AMExtendedSeekingCapabilities, AMExtendedSeekingCapabilities enumeration [DirectShow], AMExtendedSeekingCapabilitiesEnumeration, AM_EXSEEK_BUFFERING, AM_EXSEEK_CANSCAN, AM_EXSEEK_CANSEEK, AM_EXSEEK_MARKERSEEK, AM_EXSEEK_NOSTANDARDREPAINT, AM_EXSEEK_SCANWITHOUTCLOCK, AM_EXSEEK_SENDS_VIDEOFRAMEREADY, dshow.amextendedseekingcapabilities, qnetwork/AMExtendedSeekingCapabilities, qnetwork/AM_EXSEEK_BUFFERING, qnetwork/AM_EXSEEK_CANSCAN, qnetwork/AM_EXSEEK_CANSEEK, qnetwork/AM_EXSEEK_MARKERSEEK, qnetwork/AM_EXSEEK_NOSTANDARDREPAINT, qnetwork/AM_EXSEEK_SCANWITHOUTCLOCK, qnetwork/AM_EXSEEK_SENDS_VIDEOFRAMEREADY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qnetwork.h
api_name:
-	AMExtendedSeekingCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# AMExtendedSeekingCapabilities enumeration


## -description



The <b>AMExtendedSeekingCapabilities</b> enumeration contains flags that describe the extended seeking capabilities of a filter.




## -enum-fields




### -field AM_EXSEEK_CANSEEK


            Indicates that the stream is seekable.
          


### -field AM_EXSEEK_CANSCAN


            Indicates that the filter supports rates other than 1.0.
          


### -field AM_EXSEEK_MARKERSEEK


            Indicates that the stream contains markers.
          


### -field AM_EXSEEK_SCANWITHOUTCLOCK


            Indicates that the filter can play back at rates other than 1.0.
          


### -field AM_EXSEEK_NOSTANDARDREPAINT


            Indicates that the filter can seek to a new frame without displaying the new frame when it finds it.
          


### -field AM_EXSEEK_BUFFERING


            Indicates that the filter can seek while the stream is buffering.
          


### -field AM_EXSEEK_SENDS_VIDEOFRAMEREADY


            Indicates that the filter's video pin has been created.
          


## -remarks



See <a href="https://msdn.microsoft.com/caae9e8c-6d42-4bbc-a66a-bdde1009469d">IAMExtendedSeeking::get_ExSeekCapabilities</a> for descriptions of how the <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter sets these flags.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 


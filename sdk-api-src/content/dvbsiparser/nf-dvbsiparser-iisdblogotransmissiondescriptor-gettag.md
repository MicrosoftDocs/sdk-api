---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetTag
title: IIsdbLogoTransmissionDescriptor::GetTag
author: windows-driver-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor_gettag.htm
old-project: mstv
ms.assetid: 7ad7d7b5-a20f-4d03-b699-a39fe7ea7568
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbLogoTransmissionDescriptor.GetTag, IIsdbLogoTransmissionDescriptor::GetTag, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetTag, mstv.iisdblogotransmissiondescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
-	IIsdbLogoTransmissionDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbLogoTransmissionDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB logo transmission descriptors, this value is 0xCF.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9c0930f6-6c05-48c9-91e4-2abdd3355a32">IIsdbLogoTransmissionDescriptor</a>
 

 


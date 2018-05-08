---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetLogoVersion
title: IIsdbLogoTransmissionDescriptor::GetLogoVersion
author: windows-driver-content
description: Gets the value of the logo_version field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. This field contains the version number of the logo specified in the descriptor logo_id field.
old-location: mstv\iisdblogotransmissiondescriptor_getlogoversion.htm
old-project: mstv
ms.assetid: b6cc23b4-b0cf-410c-9c15-03d58e795e6b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLogoVersion, GetLogoVersion method [Microsoft TV Technologies], GetLogoVersion method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetLogoVersion method, IIsdbLogoTransmissionDescriptor.GetLogoVersion, IIsdbLogoTransmissionDescriptor::GetLogoVersion, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoVersion, mstv.iisdblogotransmissiondescriptor_getlogoversion
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
-	IIsdbLogoTransmissionDescriptor.GetLogoVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbLogoTransmissionDescriptor::GetLogoVersion


## -description


Gets the value of the logo_version field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. This field contains the version number of the logo specified in the descriptor logo_id field.


## -parameters




### -param pwVal [out]

Receives the logo version number. Call the <a href="https://msdn.microsoft.com/f4c11012-5d37-4d8f-944b-edfa50719b12">IIsdbLogoTransmissionDescriptor::GetLogoId</a> method to get the value of the logo_id field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9c0930f6-6c05-48c9-91e4-2abdd3355a32">IIsdbLogoTransmissionDescriptor</a>



<a href="https://msdn.microsoft.com/f4c11012-5d37-4d8f-944b-edfa50719b12">IIsdbLogoTransmissionDescriptor::GetLogoId</a>
 

 


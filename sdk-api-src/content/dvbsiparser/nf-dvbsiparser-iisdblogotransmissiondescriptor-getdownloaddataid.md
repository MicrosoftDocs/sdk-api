---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetDownloadDataId
title: IIsdbLogoTransmissionDescriptor::GetDownloadDataId
author: windows-sdk-content
description: Gets the value of the download_data_id field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor_getdownloaddataid.htm
tech.root: MSTV
ms.assetid: 3672458d-0f7d-4264-8362-2ddad3afecab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDownloadDataId, GetDownloadDataId method [Microsoft TV Technologies], GetDownloadDataId method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetDownloadDataId method, IIsdbLogoTransmissionDescriptor.GetDownloadDataId, IIsdbLogoTransmissionDescriptor::GetDownloadDataId, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetDownloadDataId, mstv.iisdblogotransmissiondescriptor_getdownloaddataid
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
 - IIsdbLogoTransmissionDescriptor.GetDownloadDataId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbLogoTransmissionDescriptor.GetDownloadDataId
: 
---

# IIsdbLogoTransmissionDescriptor::GetDownloadDataId


## -description


Gets the value of the download_data_id field from  an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. This field identifies the downloaded data and has the same value as the table_id_extensions field in the common data table  that contains the logo data.


## -parameters




### -param pwVal [out]

Receives the download data identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9c0930f6-6c05-48c9-91e4-2abdd3355a32">IIsdbLogoTransmissionDescriptor</a>
 

 


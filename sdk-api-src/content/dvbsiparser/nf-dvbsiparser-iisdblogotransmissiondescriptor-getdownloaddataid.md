---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetDownloadDataId
title: IIsdbLogoTransmissionDescriptor::GetDownloadDataId (dvbsiparser.h)
description: Gets the value of the download_data_id field from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor_getdownloaddataid.htm
tech.root: mstv
ms.assetid: 3672458d-0f7d-4264-8362-2ddad3afecab
ms.date: 12/05/2018
ms.keywords: GetDownloadDataId, GetDownloadDataId method [Microsoft TV Technologies], GetDownloadDataId method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetDownloadDataId method, IIsdbLogoTransmissionDescriptor.GetDownloadDataId, IIsdbLogoTransmissionDescriptor::GetDownloadDataId, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetDownloadDataId, mstv.iisdblogotransmissiondescriptor_getdownloaddataid
f1_keywords:
- dvbsiparser/IIsdbLogoTransmissionDescriptor.GetDownloadDataId
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdblogotransmissiondescriptor">IIsdbLogoTransmissionDescriptor</a>
 

 


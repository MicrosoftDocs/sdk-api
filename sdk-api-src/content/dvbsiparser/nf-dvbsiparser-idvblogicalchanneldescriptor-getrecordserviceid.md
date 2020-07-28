---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetRecordServiceId
title: IDvbLogicalChannelDescriptor::GetRecordServiceId (dvbsiparser.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.  .
helpviewer_keywords: ["GetRecordServiceId","GetRecordServiceId method [DirectShow]","GetRecordServiceId method [DirectShow]","IDvbLogicalChannelDescriptor interface","IDvbLogicalChannelDescriptor interface [DirectShow]","GetRecordServiceId method","IDvbLogicalChannelDescriptor.GetRecordServiceId","IDvbLogicalChannelDescriptor::GetRecordServiceId","IDvbLogicalChannelDescriptorGetRecordServiceId","dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordServiceId","mstv.idvblogicalchanneldescriptor_getrecordserviceid"]
old-location: mstv\idvblogicalchanneldescriptor_getrecordserviceid.htm
tech.root: mstv
ms.assetid: ab0670e9-400c-4a3f-8afa-e323a3915dc3
ms.date: 12/05/2018
ms.keywords: GetRecordServiceId, GetRecordServiceId method [DirectShow], GetRecordServiceId method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetRecordServiceId method, IDvbLogicalChannelDescriptor.GetRecordServiceId, IDvbLogicalChannelDescriptor::GetRecordServiceId, IDvbLogicalChannelDescriptorGetRecordServiceId, dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordServiceId, mstv.idvblogicalchanneldescriptor_getrecordserviceid
f1_keywords:
- dvbsiparser/IDvbLogicalChannelDescriptor.GetRecordServiceId
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- IDvbLogicalChannelDescriptor.GetRecordServiceId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbLogicalChannelDescriptor::GetRecordServiceId


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>




The <b>GetRecordServiceId</b> method returns the service identifier at a specified index in the channel list.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the service identifier to return. To get the number of service identifiers in the descriptor, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchanneldescriptor-getcountofrecords">IDvbLogicalChannelDescriptor::GetCountOfRecords</a>.
          


### -param pwVal [out]

Receives the service_id field.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a>
 

 


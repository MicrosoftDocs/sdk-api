---
UID: NF:dvbsiparser.IDvbContentIdentifierDescriptor.GetRecordCrid
title: IDvbContentIdentifierDescriptor::GetRecordCrid (dvbsiparser.h)
author: windows-sdk-content
description: Gets the content reference identifier (CRID) from a Digital Video Broadcast (DVB) content identifier descriptor.
old-location: mstv\idvbcontentidentifierdescriptor_getrecordcrid.htm
tech.root: mstv
ms.assetid: de3593a6-f39c-4c4a-9ddf-1343186d98e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordCrid, GetRecordCrid method [Microsoft TV Technologies], GetRecordCrid method [Microsoft TV Technologies],IDvbContentIdentifierDescriptor interface, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],GetRecordCrid method, IDvbContentIdentifierDescriptor.GetRecordCrid, IDvbContentIdentifierDescriptor::GetRecordCrid, dvbsiparser/IDvbContentIdentifierDescriptor::GetRecordCrid, mstv.idvbcontentidentifierdescriptor_getrecordcrid
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbContentIdentifierDescriptor.GetRecordCrid"
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
 - IDvbContentIdentifierDescriptor.GetRecordCrid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbContentIdentifierDescriptor::GetRecordCrid


## -description


Gets the content reference identifier (CRID) from a Digital Video Broadcast (DVB) content identifier descriptor.  


## -parameters




### -param bRecordIndex [in]

Zero-based index of the service record to return. To get the number of service records in the descriptor, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-getcountofrecords">IDvbContentIdentifierDescriptor::GetCountOfRecords</a> method.


### -param pbType [out]

Receives the type of the CRID. 


### -param pbLocation [out]

Gets the location of the CRID. 


### -param pbLength [out]

Gets the number of bytes required to return the CRID.


### -param ppbBytes [out]

Pointer to a buffer that receives the CRID. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentidentifierdescriptor">IDvbContentIdentifierDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-getcountofrecords">IDvbContentIdentifierDescriptor::GetCountOfRecords</a>
 

 


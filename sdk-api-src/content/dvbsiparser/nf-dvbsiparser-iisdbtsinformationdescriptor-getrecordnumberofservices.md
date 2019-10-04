---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordNumberOfServices
title: IIsdbTSInformationDescriptor::GetRecordNumberOfServices (dvbsiparser.h)
author: windows-sdk-content
description: Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_getrecordnumberofservices.htm
tech.root: mstv
ms.assetid: bf9ec856-951e-4a75-a136-9fa6eaf9e8cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordNumberOfServices, GetRecordNumberOfServices method [Microsoft TV Technologies], GetRecordNumberOfServices method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRecordNumberOfServices method, IIsdbTSInformationDescriptor.GetRecordNumberOfServices, IIsdbTSInformationDescriptor::GetRecordNumberOfServices, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordNumberOfServices, mstv.iisdbtsinformationdescriptor_getrecordnumberofservices
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbTSInformationDescriptor.GetRecordNumberOfServices"
dev_langs:
 - c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbTSInformationDescriptor.GetRecordNumberOfServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbTSInformationDescriptor::GetRecordNumberOfServices


## -description


Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives the number of service records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IIsdbTSInformationDescriptor::GetCountOfRecords</a>
 

 


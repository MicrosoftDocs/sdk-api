---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo
title: IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo
author: windows-sdk-content
description: Gets the transmission_type_info field from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_getrecordtransmissiontypeinfo.htm
old-project: mstv
ms.assetid: 992ef7de-ccf8-42a1-bb83-4b5f396164ce
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordTransmissionTypeInfo, GetRecordTransmissionTypeInfo method [Microsoft TV Technologies], GetRecordTransmissionTypeInfo method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetRecordTransmissionTypeInfo method, IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo, IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo, mstv.iisdbtsinformationdescriptor_getrecordtransmissiontypeinfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbTSInformationDescriptor.GetRecordTransmissionTypeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbTSInformationDescriptor::GetRecordTransmissionTypeInfo


## -description


Gets the transmission_type_info field from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. This field is used to select hierarchical layers within the service information and is defined by each service provider.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbTSInformationDescriptor::GetCountOfRecords</a>



### -param pbVal [out]

Receives the transmission_type_info field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>



<a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbTSInformationDescriptor::GetCountOfRecords</a>
 

 


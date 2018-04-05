---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetRecordNumberOfServices
title: IIsdbTSInformationDescriptor::GetRecordNumberOfServices method
author: windows-driver-content
description: Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
old-location: mstv\iisdbtsinformationdescriptor_getrecordnumberofservices.htm
old-project: mstv
ms.assetid: bf9ec856-951e-4a75-a136-9fa6eaf9e8cd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRecordNumberOfServices method [Microsoft TV Technologies], GetRecordNumberOfServices method [Microsoft TV Technologies], IIsdbTSInformationDescriptor interface, GetRecordNumberOfServices,IIsdbTSInformationDescriptor.GetRecordNumberOfServices, IIsdbTSInformationDescriptor, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies], GetRecordNumberOfServices method, IIsdbTSInformationDescriptor::GetRecordNumberOfServices, dvbsiparser/IIsdbTSInformationDescriptor::GetRecordNumberOfServices, mstv.iisdbtsinformationdescriptor_getrecordnumberofservices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbTSInformationDescriptor.GetRecordNumberOfServices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbTSInformationDescriptor::GetRecordNumberOfServices method


## -description


Gets the number of service records from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">IIsdbTSInformationDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives the number of service records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>



<a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">IIsdbTSInformationDescriptor::GetCountOfRecords</a>
 

 


---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetRecordComponentRef
title: IIsdbDataContentDescriptor::GetRecordComponentRef (dvbsiparser.h)
description: Gets the value of the component_ref field from a specified component record in an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field contains the broadcaster-defined component tag that identifies a component stream.
old-location: mstv\iisdbdatacontentdescriptor_getrecordcomponentref.htm
tech.root: mstv
ms.assetid: 3668c323-6808-4bc4-b372-37647ef3fdd8
ms.date: 12/05/2018
ms.keywords: GetRecordComponentRef, GetRecordComponentRef method [Microsoft TV Technologies], GetRecordComponentRef method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetRecordComponentRef method, IIsdbDataContentDescriptor.GetRecordComponentRef, IIsdbDataContentDescriptor::GetRecordComponentRef, dvbsiparser/IIsdbDataContentDescriptor::GetRecordComponentRef, mstv.iisdbdatacontentdescriptor_getrecordcomponentref
f1_keywords:
- dvbsiparser/IIsdbDataContentDescriptor.GetRecordComponentRef
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
- IIsdbDataContentDescriptor.GetRecordComponentRef
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor::GetRecordComponentRef


## -description


 Gets the value of the component_ref field from a specified component record in an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field contains the broadcaster-defined component tag that identifies a component stream. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the component record containing the tag. To get the number of components, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbDataContentDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives the component tag. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
 

 


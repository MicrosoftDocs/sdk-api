---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetStartEndFlag
title: IIsdbEmergencyInformationDescriptor::GetStartEndFlag (dvbsiparser.h)
description: Gets the value of the start_end_flag field from an emergency information descriptor. This field indicates whether the emergency alarm signal has started or finished broadcasting.
helpviewer_keywords: ["GetStartEndFlag","GetStartEndFlag method [Microsoft TV Technologies]","GetStartEndFlag method [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","GetStartEndFlag method","IIsdbEmergencyInformationDescriptor.GetStartEndFlag","IIsdbEmergencyInformationDescriptor::GetStartEndFlag","dvbsiparser/IIsdbEmergencyInformationDescriptor::GetStartEndFlag","mstv.iisdbemergencyinformationdescriptor_getstartendflag"]
old-location: mstv\iisdbemergencyinformationdescriptor_getstartendflag.htm
tech.root: mstv
ms.assetid: 13593be1-073c-41df-b389-f0920d192c92
ms.date: 12/05/2018
ms.keywords: GetStartEndFlag, GetStartEndFlag method [Microsoft TV Technologies], GetStartEndFlag method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetStartEndFlag method, IIsdbEmergencyInformationDescriptor.GetStartEndFlag, IIsdbEmergencyInformationDescriptor::GetStartEndFlag, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetStartEndFlag, mstv.iisdbemergencyinformationdescriptor_getstartendflag
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbEmergencyInformationDescriptor::GetStartEndFlag
 - dvbsiparser/IIsdbEmergencyInformationDescriptor::GetStartEndFlag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbEmergencyInformationDescriptor.GetStartEndFlag
---

# IIsdbEmergencyInformationDescriptor::GetStartEndFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the value of the start_end_flag field from an emergency information descriptor. This field indicates whether the emergency alarm signal has started or finished broadcasting.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the service information (SI) descriptor containing the table descriptor. To get the number of SI descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>

### -param pVal [out]

Gets the start/end flag from the descriptor. If this value is 1, the emergency signal has started or is being broadcast. If it is 0, the emergency signal broadcast has ended.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbemergencyinformationdescriptor">IIsdbEmergencyInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetSignalLevel
title: IIsdbEmergencyInformationDescriptor::GetSignalLevel (dvbsiparser.h)
description: Gets a flag that indicates the emergency alarm signal type from an emergency information descriptor.
helpviewer_keywords: ["GetSignalLevel","GetSignalLevel method [Microsoft TV Technologies]","GetSignalLevel method [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","GetSignalLevel method","IIsdbEmergencyInformationDescriptor.GetSignalLevel","IIsdbEmergencyInformationDescriptor::GetSignalLevel","dvbsiparser/IIsdbEmergencyInformationDescriptor::GetSignalLevel","mstv.iisdbemergencyinformationdescriptor_getsignallevel"]
old-location: mstv\iisdbemergencyinformationdescriptor_getsignallevel.htm
tech.root: mstv
ms.assetid: cf0c8d51-4ec8-4dad-8ef3-f18339ed0c0c
ms.date: 12/05/2018
ms.keywords: GetSignalLevel, GetSignalLevel method [Microsoft TV Technologies], GetSignalLevel method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetSignalLevel method, IIsdbEmergencyInformationDescriptor.GetSignalLevel, IIsdbEmergencyInformationDescriptor::GetSignalLevel, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetSignalLevel, mstv.iisdbemergencyinformationdescriptor_getsignallevel
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
 - IIsdbEmergencyInformationDescriptor::GetSignalLevel
 - dvbsiparser/IIsdbEmergencyInformationDescriptor::GetSignalLevel
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
 - IIsdbEmergencyInformationDescriptor.GetSignalLevel
---

# IIsdbEmergencyInformationDescriptor::GetSignalLevel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a flag that indicates the emergency alarm signal type from an emergency information descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the emergency information descriptor that contains the emergency alarm signal. To get the number of emergency information descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>.

### -param pbVal [out]

Receives a boolean value that indicates whether the emergency alarm signal is the first (0) or second (1) type of start signal. Annex D of the document titled <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM,
ARIB STANDARD,
ARIB STD-B10, Version 4.4</i> describes the two start signal types.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbemergencyinformationdescriptor">IIsdbEmergencyInformationDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">IIsdbEmergencyInformationDescriptor::GetCountOfRecords</a>
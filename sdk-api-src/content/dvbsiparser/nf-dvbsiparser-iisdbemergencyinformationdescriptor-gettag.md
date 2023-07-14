---
UID: NF:dvbsiparser.IIsdbEmergencyInformationDescriptor.GetTag
title: IIsdbEmergencyInformationDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an emergency information descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbEmergencyInformationDescriptor.GetTag","IIsdbEmergencyInformationDescriptor::GetTag","dvbsiparser/IIsdbEmergencyInformationDescriptor::GetTag","mstv.iisdbemergencyinformationdescriptor_gettag"]
old-location: mstv\iisdbemergencyinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: d0751a09-0336-48d7-a5f0-1182354774a4
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbEmergencyInformationDescriptor interface, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbEmergencyInformationDescriptor.GetTag, IIsdbEmergencyInformationDescriptor::GetTag, dvbsiparser/IIsdbEmergencyInformationDescriptor::GetTag, mstv.iisdbemergencyinformationdescriptor_gettag
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
 - IIsdbEmergencyInformationDescriptor::GetTag
 - dvbsiparser/IIsdbEmergencyInformationDescriptor::GetTag
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
 - IIsdbEmergencyInformationDescriptor.GetTag
---

# IIsdbEmergencyInformationDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an emergency information descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For emergency information descriptors, this value is 0xFC.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbemergencyinformationdescriptor">IIsdbEmergencyInformationDescriptor</a>
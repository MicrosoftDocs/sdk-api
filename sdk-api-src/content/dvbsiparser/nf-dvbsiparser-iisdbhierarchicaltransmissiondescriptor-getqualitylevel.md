---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel
title: IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel (dvbsiparser.h)
description: Gets the value of the quality_flag field from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. This field indicates the quality level of the hierarchical stream construction.
helpviewer_keywords: ["GetQualityLevel","GetQualityLevel method [Microsoft TV Technologies]","GetQualityLevel method [Microsoft TV Technologies]","IIsdbHierarchicalTransmissionDescriptor interface","IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies]","GetQualityLevel method","IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel","IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel","dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel","mstv.iisdbhierarchicaltransmissiondescriptor_getqualitylevel"]
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_getqualitylevel.htm
tech.root: mstv
ms.assetid: 4890c3aa-487f-41c7-9202-636ded2ec46b
ms.date: 12/05/2018
ms.keywords: GetQualityLevel, GetQualityLevel method [Microsoft TV Technologies], GetQualityLevel method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetQualityLevel method, IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel, IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel, mstv.iisdbhierarchicaltransmissiondescriptor_getqualitylevel
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
 - IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel
 - dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel
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
 - IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel
---

# IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the quality_flag field  from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. This field indicates the quality level of the hierarchical stream construction.

## -parameters

### -param pbVal [out]

Receives the quality_flag field value. A value of 1 indicates a high-quality stream; a value of 0 indicates a low-quality stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbhierarchicaltransmissiondescriptor">IIsdbHierarchicalTransmissionDescriptor</a>
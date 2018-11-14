---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel
title: IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel
author: windows-sdk-content
description: Gets the value of the quality_flag field from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. This field indicates the quality level of the hierarchical stream construction.
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_getqualitylevel.htm
tech.root: MSTV
ms.assetid: 4890c3aa-487f-41c7-9202-636ded2ec46b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetQualityLevel, GetQualityLevel method [Microsoft TV Technologies], GetQualityLevel method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetQualityLevel method, IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel, IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel, mstv.iisdbhierarchicaltransmissiondescriptor_getqualitylevel
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IIsdbHierarchicalTransmissionDescriptor.GetQualityLevel
: 
---

# IIsdbHierarchicalTransmissionDescriptor::GetQualityLevel


## -description


Gets the value of the quality_flag field  from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor. This field indicates the quality level of the hierarchical stream construction.


## -parameters




### -param pbVal [out]

Receives the quality_flag field value. A value of 1 indicates a high-quality stream; a value of 0 indicates a low-quality stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6586360b-60d8-4c3c-aa6e-b657e1784b6d">IIsdbHierarchicalTransmissionDescriptor</a>
 

 


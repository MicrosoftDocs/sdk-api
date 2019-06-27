---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetTag
title: IIsdbHierarchicalTransmissionDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a hierarchical transmission descriptor.
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_gettag.htm
tech.root: mstv
ms.assetid: 1aed2424-567b-4a6b-ae32-b3c74ce75026
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbHierarchicalTransmissionDescriptor.GetTag, IIsdbHierarchicalTransmissionDescriptor::GetTag, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetTag, mstv.iisdbhierarchicaltransmissiondescriptor_gettag
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbHierarchicalTransmissionDescriptor.GetTag"
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
 - IIsdbHierarchicalTransmissionDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbHierarchicalTransmissionDescriptor::GetTag


## -description


Gets the tag that identifies a hierarchical transmission descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For hierarchical transmission descriptors, this value is 0xC0.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbhierarchicaltransmissiondescriptor">IIsdbHierarchicalTransmissionDescriptor</a>
 

 


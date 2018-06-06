---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetTag
title: IIsdbHierarchicalTransmissionDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a hierarchical transmission descriptor.
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_gettag.htm
old-project: mstv
ms.assetid: 1aed2424-567b-4a6b-ae32-b3c74ce75026
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbHierarchicalTransmissionDescriptor.GetTag, IIsdbHierarchicalTransmissionDescriptor::GetTag, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetTag, mstv.iisdbhierarchicaltransmissiondescriptor_gettag
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
 - IIsdbHierarchicalTransmissionDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/6586360b-60d8-4c3c-aa6e-b657e1784b6d">IIsdbHierarchicalTransmissionDescriptor</a>
 

 


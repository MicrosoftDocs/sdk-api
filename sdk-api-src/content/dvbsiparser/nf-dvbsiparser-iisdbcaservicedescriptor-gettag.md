---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetTag
title: IIsdbCAServiceDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a conditional access (CA) service descriptor.helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbCAServiceDescriptor.GetTag","IIsdbCAServiceDescriptor::GetTag","dvbsiparser/IIsdbCAServiceDescriptor::GetTag","mstv.iisdbcaservicedescriptor_gettag"]
old-location: mstv\iisdbcaservicedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 55f7b955-03f6-4c40-bd73-175bf3453ed0
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCAServiceDescriptor.GetTag, IIsdbCAServiceDescriptor::GetTag, dvbsiparser/IIsdbCAServiceDescriptor::GetTag, mstv.iisdbcaservicedescriptor_gettag
f1_keywords:
- dvbsiparser/IIsdbCAServiceDescriptor.GetTag
dev_langs:
- c++
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
- IIsdbCAServiceDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAServiceDescriptor::GetTag


## -description


Gets the tag that identifies a conditional access (CA) service descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For conditional access service descriptors, this value is 0xCC.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>
 

 


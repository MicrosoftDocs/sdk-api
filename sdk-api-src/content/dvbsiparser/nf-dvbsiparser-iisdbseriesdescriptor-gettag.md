---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetTag
title: IIsdbSeriesDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) series descriptor.helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbSeriesDescriptor.GetTag","IIsdbSeriesDescriptor::GetTag","dvbsiparser/IIsdbSeriesDescriptor::GetTag","mstv.iisdbseriesdescriptor_gettag"]
old-location: mstv\iisdbseriesdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 7f67fcf4-76b6-4e1c-99a1-e09b406b5bd9
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbSeriesDescriptor.GetTag, IIsdbSeriesDescriptor::GetTag, dvbsiparser/IIsdbSeriesDescriptor::GetTag, mstv.iisdbseriesdescriptor_gettag
f1_keywords:
- dvbsiparser/IIsdbSeriesDescriptor.GetTag
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
- IIsdbSeriesDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbSeriesDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) series descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB series descriptors, this value is 0xD5.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>
 

 


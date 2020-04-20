---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetTag
title: IIsdbDataContentDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) data content descriptor.helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbDataContentDescriptor.GetTag","IIsdbDataContentDescriptor::GetTag","dvbsiparser/IIsdbDataContentDescriptor::GetTag","mstv.iisdbdatacontentdescriptor_gettag"]
old-location: mstv\iisdbdatacontentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 308f44d6-0aae-418e-8aad-cc812c0cdb8a
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbDataContentDescriptor.GetTag, IIsdbDataContentDescriptor::GetTag, dvbsiparser/IIsdbDataContentDescriptor::GetTag, mstv.iisdbdatacontentdescriptor_gettag
f1_keywords:
- dvbsiparser/IIsdbDataContentDescriptor.GetTag
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
- IIsdbDataContentDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) data content descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB data content descriptors, this value is 0xC7.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
 

 


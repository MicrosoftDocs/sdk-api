---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetTag
title: IDvbTeletextDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that idenfities a Digital Video Broadcast (DVB) teletext descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbTeletextDescriptor interface","IDvbTeletextDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbTeletextDescriptor.GetTag","IDvbTeletextDescriptor::GetTag","dvbsiparser/IDvbTeletextDescriptor::GetTag","mstv.idvbteletextdescriptor_gettag"]
old-location: mstv\idvbteletextdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 1f359c37-8d8f-48de-a4a2-89617c5761ed
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbTeletextDescriptor.GetTag, IDvbTeletextDescriptor::GetTag, dvbsiparser/IDvbTeletextDescriptor::GetTag, mstv.idvbteletextdescriptor_gettag
f1_keywords:
- dvbsiparser/IDvbTeletextDescriptor.GetTag
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
- IDvbTeletextDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbTeletextDescriptor::GetTag


## -description


Gets the tag that idenfities a Digital Video Broadcast (DVB) teletext descriptor.
  


## -parameters




### -param pbVal [out]

Gets the tag for the teletext descriptor. For teletext descriptors, this value is 0x56.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>
 

 


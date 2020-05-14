---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetEntryComponent
title: IIsdbDataContentDescriptor::GetEntryComponent (dvbsiparser.h)
description: Gets the value of the entry_component field from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field indicates the first component stream that is referenced in the descriptor.helpviewer_keywords: ["GetEntryComponent","GetEntryComponent method [Microsoft TV Technologies]","GetEntryComponent method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetEntryComponent method","IIsdbDataContentDescriptor.GetEntryComponent","IIsdbDataContentDescriptor::GetEntryComponent","dvbsiparser/IIsdbDataContentDescriptor::GetEntryComponent","mstv.iisdbdatacontentdescriptor_getentrycomponent"]
old-location: mstv\iisdbdatacontentdescriptor_getentrycomponent.htm
tech.root: mstv
ms.assetid: 9f8f9e55-cc03-4f07-918e-19199485c8d4
ms.date: 12/05/2018
ms.keywords: GetEntryComponent, GetEntryComponent method [Microsoft TV Technologies], GetEntryComponent method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetEntryComponent method, IIsdbDataContentDescriptor.GetEntryComponent, IIsdbDataContentDescriptor::GetEntryComponent, dvbsiparser/IIsdbDataContentDescriptor::GetEntryComponent, mstv.iisdbdatacontentdescriptor_getentrycomponent
f1_keywords:
- dvbsiparser/IIsdbDataContentDescriptor.GetEntryComponent
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
- IIsdbDataContentDescriptor.GetEntryComponent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDataContentDescriptor::GetEntryComponent


## -description


 Gets the value of the entry_component field from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field indicates the first component stream that is referenced in the descriptor.


## -parameters




### -param pbVal [out]

Returns the entry_component field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
 

 


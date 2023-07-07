---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetDataComponentId
title: IIsdbDataContentDescriptor::GetDataComponentId (dvbsiparser.h)
description: Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the data component descriptor for the component.
helpviewer_keywords: ["GetDataComponentId","GetDataComponentId method [Microsoft TV Technologies]","GetDataComponentId method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetDataComponentId method","IIsdbDataContentDescriptor.GetDataComponentId","IIsdbDataContentDescriptor::GetDataComponentId","dvbsiparser/IIsdbDataContentDescriptor::GetDataComponentId","mstv.iisdbdatacontentdescriptor_getdatacomponentid"]
old-location: mstv\iisdbdatacontentdescriptor_getdatacomponentid.htm
tech.root: mstv
ms.assetid: d8a3e399-5004-41ee-a7eb-4c583a1fdd45
ms.date: 12/05/2018
ms.keywords: GetDataComponentId, GetDataComponentId method [Microsoft TV Technologies], GetDataComponentId method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetDataComponentId method, IIsdbDataContentDescriptor.GetDataComponentId, IIsdbDataContentDescriptor::GetDataComponentId, dvbsiparser/IIsdbDataContentDescriptor::GetDataComponentId, mstv.iisdbdatacontentdescriptor_getdatacomponentid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbDataContentDescriptor::GetDataComponentId
 - dvbsiparser/IIsdbDataContentDescriptor::GetDataComponentId
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
 - IIsdbDataContentDescriptor.GetDataComponentId
---

# IIsdbDataContentDescriptor::GetDataComponentId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a data component identifier from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This identifier identifies a component in the descriptor and appears in the  data component descriptor for the component.

## -parameters

### -param pwVal [out]

Receives the data component identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
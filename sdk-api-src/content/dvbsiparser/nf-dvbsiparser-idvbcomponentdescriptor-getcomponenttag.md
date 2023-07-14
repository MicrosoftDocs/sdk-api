---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetComponentTag
title: IDvbComponentDescriptor::GetComponentTag (dvbsiparser.h)
description: Gets the component tag from a DVB component descriptor. The component tag has the same value as the component_tag field in the stream identifier descriptor in the Program Specific Information (PSI) program map section for the component stream.
helpviewer_keywords: ["GetComponentTag","GetComponentTag method [Microsoft TV Technologies]","GetComponentTag method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetComponentTag method","IDvbComponentDescriptor.GetComponentTag","IDvbComponentDescriptor::GetComponentTag","dvbsiparser/IDvbComponentDescriptor::GetComponentTag","mstv.idvbcomponentdescriptor_getcomponenttag"]
old-location: mstv\idvbcomponentdescriptor_getcomponenttag.htm
tech.root: mstv
ms.assetid: 1ecfb7db-2fb6-4389-8f62-3d912ffc301b
ms.date: 12/05/2018
ms.keywords: GetComponentTag, GetComponentTag method [Microsoft TV Technologies], GetComponentTag method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetComponentTag method, IDvbComponentDescriptor.GetComponentTag, IDvbComponentDescriptor::GetComponentTag, dvbsiparser/IDvbComponentDescriptor::GetComponentTag, mstv.idvbcomponentdescriptor_getcomponenttag
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
 - IDvbComponentDescriptor::GetComponentTag
 - dvbsiparser/IDvbComponentDescriptor::GetComponentTag
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
 - IDvbComponentDescriptor.GetComponentTag
---

# IDvbComponentDescriptor::GetComponentTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the component tag from a DVB component descriptor. The component tag has the same value as the component_tag field in the stream identifier descriptor  in the Program Specific Information (PSI) program map section for the component stream.

## -parameters

### -param pbVal [out]

Receives the component tag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>
---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetNumberOfElements
title: IServiceLocationDescriptor::GetNumberOfElements (atscpsipparser.h)
description: Gets the number of elementary streams for an Advanced Television Systems Committee (ATSC) service location descriptor.
helpviewer_keywords: ["GetNumberOfElements","GetNumberOfElements method [Microsoft TV Technologies]","GetNumberOfElements method [Microsoft TV Technologies]","IServiceLocationDescriptor interface","IServiceLocationDescriptor interface [Microsoft TV Technologies]","GetNumberOfElements method","IServiceLocationDescriptor.GetNumberOfElements","IServiceLocationDescriptor::GetNumberOfElements","atscpsipparser/IServiceLocationDescriptor::GetNumberOfElements","mstv.iservicelocationdescriptor_getnumberofelements"]
old-location: mstv\iservicelocationdescriptor_getnumberofelements.htm
tech.root: mstv
ms.assetid: 134e4051-6a73-4420-b12d-3171738bd8ad
ms.date: 12/05/2018
ms.keywords: GetNumberOfElements, GetNumberOfElements method [Microsoft TV Technologies], GetNumberOfElements method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetNumberOfElements method, IServiceLocationDescriptor.GetNumberOfElements, IServiceLocationDescriptor::GetNumberOfElements, atscpsipparser/IServiceLocationDescriptor::GetNumberOfElements, mstv.iservicelocationdescriptor_getnumberofelements
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
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
 - IServiceLocationDescriptor::GetNumberOfElements
 - atscpsipparser/IServiceLocationDescriptor::GetNumberOfElements
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IServiceLocationDescriptor.GetNumberOfElements
---

# IServiceLocationDescriptor::GetNumberOfElements


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of elementary streams for an Advanced Television Systems Committee (ATSC) service location descriptor.

## -parameters

### -param pbVal [out]

Receives the number of elementary streams.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iservicelocationdescriptor">IServiceLocationDescriptor</a>
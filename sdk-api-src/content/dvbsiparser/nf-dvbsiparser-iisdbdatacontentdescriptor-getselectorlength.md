---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetSelectorLength
title: IIsdbDataContentDescriptor::GetSelectorLength (dvbsiparser.h)
description: Gets the length of the selector part of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.
helpviewer_keywords: ["GetSelectorLength","GetSelectorLength method [Microsoft TV Technologies]","GetSelectorLength method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetSelectorLength method","IIsdbDataContentDescriptor.GetSelectorLength","IIsdbDataContentDescriptor::GetSelectorLength","dvbsiparser/IIsdbDataContentDescriptor::GetSelectorLength","mstv.iisdbdatacontentdescriptor_getselectorlength"]
old-location: mstv\iisdbdatacontentdescriptor_getselectorlength.htm
tech.root: mstv
ms.assetid: 485ac963-e85a-41cc-adcd-93590b327061
ms.date: 12/05/2018
ms.keywords: GetSelectorLength, GetSelectorLength method [Microsoft TV Technologies], GetSelectorLength method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetSelectorLength method, IIsdbDataContentDescriptor.GetSelectorLength, IIsdbDataContentDescriptor::GetSelectorLength, dvbsiparser/IIsdbDataContentDescriptor::GetSelectorLength, mstv.iisdbdatacontentdescriptor_getselectorlength
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
 - IIsdbDataContentDescriptor::GetSelectorLength
 - dvbsiparser/IIsdbDataContentDescriptor::GetSelectorLength
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
 - IIsdbDataContentDescriptor.GetSelectorLength
---

# IIsdbDataContentDescriptor::GetSelectorLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of the selector part of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the selector length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>
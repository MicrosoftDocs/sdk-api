---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetLength
title: IIsdbEventGroupDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) event group descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbEventGroupDescriptor interface","IIsdbEventGroupDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbEventGroupDescriptor.GetLength","IIsdbEventGroupDescriptor::GetLength","dvbsiparser/IIsdbEventGroupDescriptor::GetLength","mstv.iisdbeventgroupdescriptor_getlength"]
old-location: mstv\iisdbeventgroupdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 08e61ddb-15d5-40e3-9e37-7c45d1f18b4a
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbEventGroupDescriptor.GetLength, IIsdbEventGroupDescriptor::GetLength, dvbsiparser/IIsdbEventGroupDescriptor::GetLength, mstv.iisdbeventgroupdescriptor_getlength
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
 - IIsdbEventGroupDescriptor::GetLength
 - dvbsiparser/IIsdbEventGroupDescriptor::GetLength
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
 - IIsdbEventGroupDescriptor.GetLength
---

# IIsdbEventGroupDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) event group descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>
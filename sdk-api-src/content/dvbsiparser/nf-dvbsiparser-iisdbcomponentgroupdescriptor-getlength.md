---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetLength
title: IIsdbComponentGroupDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) component group descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbComponentGroupDescriptor.GetLength","IIsdbComponentGroupDescriptor::GetLength","dvbsiparser/IIsdbComponentGroupDescriptor::GetLength","mstv.iisdbcomponentgroupdescriptor_getlength"]
old-location: mstv\iisdbcomponentgroupdescriptor_getlength.htm
tech.root: mstv
ms.assetid: a499d259-460c-428b-ba96-63f71eb556fa
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbComponentGroupDescriptor.GetLength, IIsdbComponentGroupDescriptor::GetLength, dvbsiparser/IIsdbComponentGroupDescriptor::GetLength, mstv.iisdbcomponentgroupdescriptor_getlength
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
 - IIsdbComponentGroupDescriptor::GetLength
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetLength
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
 - IIsdbComponentGroupDescriptor.GetLength
---

# IIsdbComponentGroupDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) component group descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getlength">IIsdbComponentGroupDescriptor</a>
---
UID: NF:dvbsiparser.IIsdbDigitalCopyControlDescriptor.GetTag
title: IIsdbDigitalCopyControlDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbDigitalCopyControlDescriptor interface","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbDigitalCopyControlDescriptor.GetTag","IIsdbDigitalCopyControlDescriptor::GetTag","dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetTag","mstv.iisdbdigitalcopycontroldescriptor_gettag"]
old-location: mstv\iisdbdigitalcopycontroldescriptor_gettag.htm
tech.root: mstv
ms.assetid: 9e14cb87-3669-4fdf-9c84-b7f2e3c840c2
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbDigitalCopyControlDescriptor interface, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbDigitalCopyControlDescriptor.GetTag, IIsdbDigitalCopyControlDescriptor::GetTag, dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetTag, mstv.iisdbdigitalcopycontroldescriptor_gettag
f1_keywords:
- dvbsiparser/IIsdbDigitalCopyControlDescriptor.GetTag
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
- IIsdbDigitalCopyControlDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDigitalCopyControlDescriptor::GetTag


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For a digital copy control descriptor, this value is 0xC1.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdigitalcopycontroldescriptor">IIsdbDigitalCopyControlDescriptor</a>
 

 


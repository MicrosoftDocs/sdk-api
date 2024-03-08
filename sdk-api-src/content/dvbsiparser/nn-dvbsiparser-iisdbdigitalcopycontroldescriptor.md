---
UID: NN:dvbsiparser.IIsdbDigitalCopyControlDescriptor
title: IIsdbDigitalCopyControlDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.
helpviewer_keywords: ["IIsdbDigitalCopyControlDescriptor","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbDigitalCopyControlDescriptor","mstv.iisdbdigitalcopycontroldescriptor"]
old-location: mstv\iisdbdigitalcopycontroldescriptor.htm
tech.root: mstv
ms.assetid: d509eb58-0c58-4173-8c9c-d52b81932b5c
ms.date: 12/05/2018
ms.keywords: IIsdbDigitalCopyControlDescriptor, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies], IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDigitalCopyControlDescriptor, mstv.iisdbdigitalcopycontroldescriptor
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
 - IIsdbDigitalCopyControlDescriptor
 - dvbsiparser/IIsdbDigitalCopyControlDescriptor
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
 - IIsdbDigitalCopyControlDescriptor
---

# IIsdbDigitalCopyControlDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor. The digital copy control descriptor appears in the ISDB Service Information as part of the event information table (EIT). Broadcasting service
providers who hold copyrights can use this descriptor to provide data that controls the recording of digital broadcasts and provides copyright data for digital recording equipment. This descriptor also identifies the maximum transmission rate
for each event.

## -inheritance

The <b>IIsdbDigitalCopyControlDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbDigitalCopyControlDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>


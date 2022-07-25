---
UID: NN:bdaiface.IEnumPIDMap
title: IEnumPIDMap (bdaiface.h)
description: The IEnumPIDMap interface enumerates a collection of Packet ID (PID) maps.
helpviewer_keywords: ["IEnumPIDMap","IEnumPIDMap interface [DirectShow]","IEnumPIDMap interface [DirectShow]","described","IEnumPIDMapInterface","bdaiface/IEnumPIDMap","dshow.ienumpidmap"]
old-location: dshow\ienumpidmap.htm
tech.root: dshow
ms.assetid: d46010c4-0f16-4c97-ad10-16f7ac250390
ms.date: 12/05/2018
ms.keywords: IEnumPIDMap, IEnumPIDMap interface [DirectShow], IEnumPIDMap interface [DirectShow],described, IEnumPIDMapInterface, bdaiface/IEnumPIDMap, dshow.ienumpidmap
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumPIDMap
 - bdaiface/IEnumPIDMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumPIDMap
---

# IEnumPIDMap interface


## -description

The <code>IEnumPIDMap</code> interface enumerates a collection of Packet ID (PID) maps. Each PID map describes how the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> filter maps a PID to an output pin on the filter. PID mappings are created by calling the <a href="/previous-versions/windows/desktop/api/bdaiface/nf-bdaiface-impeg2pidmap-mappid">IMPEG2PIDMap::MapPID</a> method on the filter's output pin.

To obtain the <code>IEnumPIDMap</code> interface, call the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-impeg2pidmap-enumpidmap">IMPEG2PIDMap::EnumPIDMap</a> method on the output pin. Typically, output pins for audio and video streams have at most one PID mapped at any given time.

This interface implements a standard Component Object Model (COM) collection object. The collection object represents a snapshot of the PID map when the collection is created. The collection is not updated automatically.

## -inheritance

The <b>IEnumPIDMap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPIDMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>


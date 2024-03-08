---
UID: NN:sbe.IEnumStreamBufferRecordingAttrib
title: IEnumStreamBufferRecordingAttrib (sbe.h)
description: The IEnumStreamBufferRecordingAttrib interface enumerates a collection of attributes on a stream buffer file.
helpviewer_keywords: ["IEnumStreamBufferRecordingAttrib","IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies]","IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies]","described","IEnumStreamBufferRecordingAttribInterface","mstv.ienumstreambufferrecordingattrib","sbe/IEnumStreamBufferRecordingAttrib"]
old-location: mstv\ienumstreambufferrecordingattrib.htm
tech.root: mstv
ms.assetid: 668d2e04-74fa-41d7-b238-ec737a4441ca
ms.date: 12/05/2018
ms.keywords: IEnumStreamBufferRecordingAttrib, IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies], IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],described, IEnumStreamBufferRecordingAttribInterface, mstv.ienumstreambufferrecordingattrib, sbe/IEnumStreamBufferRecordingAttrib
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IEnumStreamBufferRecordingAttrib
 - sbe/IEnumStreamBufferRecordingAttrib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IEnumStreamBufferRecordingAttrib
---

# IEnumStreamBufferRecordingAttrib interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEnumStreamBufferRecordingAttrib</b> interface enumerates a collection of attributes on a stream buffer file. <i>Attributes</i> are metadata that describe the physical file (such as the bit rate and the duration) or the content of the file (such as the author or title). To obtain this interface, call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-enumattributes">IStreamBufferRecordingAttribute::EnumAttributes</a> method.

This interface implements a standard Component Object Model (COM) collection object. For more information on COM collections, see the <b>IEnumXXXX</b> topic in the Microsoft Platform SDK. The collection object represents a snapshot of the attributes when the collection is created; the collection is not updated automatically.

## -inheritance

The <b>IEnumStreamBufferRecordingAttrib</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumStreamBufferRecordingAttrib</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumStreamBufferRecordingAttrib)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>

---
UID: NN:sbe.IStreamBufferRecordingAttribute
title: IStreamBufferRecordingAttribute (sbe.h)
description: The IStreamBufferRecordingAttribute interface sets and retrieves attributes on a stream buffer recording.
helpviewer_keywords: ["IStreamBufferRecordingAttribute","IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","described","IStreamBufferRecordingAttributeInterface","mstv.istreambufferrecordingattribute","sbe/IStreamBufferRecordingAttribute"]
old-location: mstv\istreambufferrecordingattribute.htm
tech.root: mstv
ms.assetid: 7c46413f-3e51-4d72-b7f7-a8239c61b161
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordingAttribute, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies], IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],described, IStreamBufferRecordingAttributeInterface, mstv.istreambufferrecordingattribute, sbe/IStreamBufferRecordingAttribute
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
 - IStreamBufferRecordingAttribute
 - sbe/IStreamBufferRecordingAttribute
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
 - IStreamBufferRecordingAttribute
---

# IStreamBufferRecordingAttribute interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferRecordingAttribute</b> interface sets and retrieves attributes on a stream buffer recording. <i>Attributes</i> are metadata that describe the physical file (such as the bitrate and the duration) or the content of the file (such as the author or title).

This interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/recording-object">Recording</a> object and the <a href="/previous-versions/windows/desktop/mstv/recordingattributes-object">RecordingAttributes</a> object.

## -inheritance

The <b>IStreamBufferRecordingAttribute</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecordingAttribute</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordingAttribute)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-attributes">Stream Buffer Engine Attributes</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>

---
UID: NN:wmcontainer.IMFASFSplitter
title: IMFASFSplitter (wmcontainer.h)
description: Provides methods to read data from an Advanced Systems Format (ASF) file.
helpviewer_keywords: ["75d8b2a3-7c50-4dd5-8927-b11eb9f12602","IMFASFSplitter","IMFASFSplitter interface [Media Foundation]","IMFASFSplitter interface [Media Foundation]","described","mf.imfasfsplitter","wmcontainer/IMFASFSplitter"]
old-location: mf\imfasfsplitter.htm
tech.root: mf
ms.assetid: 75d8b2a3-7c50-4dd5-8927-b11eb9f12602
ms.date: 12/05/2018
ms.keywords: 75d8b2a3-7c50-4dd5-8927-b11eb9f12602, IMFASFSplitter, IMFASFSplitter interface [Media Foundation], IMFASFSplitter interface [Media Foundation],described, mf.imfasfsplitter, wmcontainer/IMFASFSplitter
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFSplitter
 - wmcontainer/IMFASFSplitter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter
---

# IMFASFSplitter interface


## -description

Provides methods to read data from an Advanced Systems Format (ASF) file. The ASF splitter object exposes this interface. To create the ASF splitter, <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter">MFCreateASFSplitter</a>.

## -inheritance

The <b>IMFASFSplitter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFSplitter</b> also has these types of members:

## -remarks

The ASF splitter accepts ASF packets and extracts the samples for individual streams from them. As with the other ASF base components, the ASF splitter object must be initialized with data from an ASF ContentInfo object before use.

## -see-also

<a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

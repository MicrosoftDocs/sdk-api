---
UID: NN:mfidl.IMFSaveJob
title: IMFSaveJob (mfidl.h)
description: Persists media data from a source byte stream to an application-provided byte stream.
helpviewer_keywords: ["0f38fa60-ed04-40c4-9bb0-b6e196cd9586","IMFSaveJob","IMFSaveJob interface [Media Foundation]","IMFSaveJob interface [Media Foundation]","described","mf.imfsavejob","mfidl/IMFSaveJob"]
old-location: mf\imfsavejob.htm
tech.root: mf
ms.assetid: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586
ms.date: 12/05/2018
ms.keywords: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586, IMFSaveJob, IMFSaveJob interface [Media Foundation], IMFSaveJob interface [Media Foundation],described, mf.imfsavejob, mfidl/IMFSaveJob
req.header: mfidl.h
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
 - IMFSaveJob
 - mfidl/IMFSaveJob
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
 - IMFSaveJob
---

# IMFSaveJob interface


## -description

Persists media data from a source byte stream to an application-provided byte stream.

The byte stream used for HTTP download implements this interface. To get a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the byte stream, with the service identifier MFNET_SAVEJOB_SERVICE.

## -inheritance

The <b>IMFSaveJob</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSaveJob</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

---
UID: NN:mfidl.IMFFinalizableMediaSink
title: IMFFinalizableMediaSink (mfidl.h)
description: Optionally supported by media sinks to perform required tasks before shutdown.
helpviewer_keywords: ["IMFFinalizableMediaSink","IMFFinalizableMediaSink interface [Media Foundation]","IMFFinalizableMediaSink interface [Media Foundation]","described","e60c2773-f2fc-469e-a698-036390cbed16","mf.imffinalizablemediasink","mfidl/IMFFinalizableMediaSink"]
old-location: mf\imffinalizablemediasink.htm
tech.root: mf
ms.assetid: e60c2773-f2fc-469e-a698-036390cbed16
ms.date: 12/05/2018
ms.keywords: IMFFinalizableMediaSink, IMFFinalizableMediaSink interface [Media Foundation], IMFFinalizableMediaSink interface [Media Foundation],described, e60c2773-f2fc-469e-a698-036390cbed16, mf.imffinalizablemediasink, mfidl/IMFFinalizableMediaSink
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
 - IMFFinalizableMediaSink
 - mfidl/IMFFinalizableMediaSink
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
 - IMFFinalizableMediaSink
---

# IMFFinalizableMediaSink interface


## -description

Optionally supported by media sinks to perform required tasks before shutdown. This interface is typically exposed by archive sinks—that is, media sinks that write to a file. It is used to perform tasks such as flushing data to disk or updating a file header.

To get a pointer to this interface, call <b>QueryInterface</b> on the media sink.

## -inheritance

The <b>IMFFinalizableMediaSink</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>. <b>IMFFinalizableMediaSink</b> also has these types of members:

## -remarks

If a media sink exposes this interface, the Media Session will call <a href="/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">BeginFinalize</a> on the sink before the session closes.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

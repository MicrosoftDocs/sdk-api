---
UID: NF:imapi2.DDiscFormat2TrackAtOnceEvents.Update
title: DDiscFormat2TrackAtOnceEvents::Update (imapi2.h)
description: Implement this method to receive progress notification of the current track-writing operation.
helpviewer_keywords: ["DDiscFormat2TrackAtOnceEvents interface [IMAPI]","Update method","DDiscFormat2TrackAtOnceEvents.Update","DDiscFormat2TrackAtOnceEvents::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DDiscFormat2TrackAtOnceEvents interface","imapi.ddiscformat2trackatonceevents_update","imapi2/DDiscFormat2TrackAtOnceEvents::Update"]
old-location: imapi\ddiscformat2trackatonceevents_update.htm
tech.root: imapi
ms.assetid: d63ff41d-993c-4f42-a4a3-f7c67f292a03
ms.date: 12/05/2018
ms.keywords: DDiscFormat2TrackAtOnceEvents interface [IMAPI],Update method, DDiscFormat2TrackAtOnceEvents.Update, DDiscFormat2TrackAtOnceEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2TrackAtOnceEvents interface, imapi.ddiscformat2trackatonceevents_update, imapi2/DDiscFormat2TrackAtOnceEvents::Update
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - DDiscFormat2TrackAtOnceEvents::Update
 - imapi2/DDiscFormat2TrackAtOnceEvents::Update
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2TrackAtOnceEvents.Update
---

# DDiscFormat2TrackAtOnceEvents::Update


## -description

Implement this method to receive progress notification of the current track-writing operation.

## -parameters

### -param object [in]

The <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2TrackAtOnce</b> object in script.

### -param progress [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs">IDiscFormat2TrackAtOnceEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2TrackAtOnce</b> object in script.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-addaudiotrack">IDiscFormat2TrackAtOnce::AddAudioTrack</a> method.

To stop the write process, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-canceladdtrack">IDiscFormat2TrackAtOnce::CancelAddTrack</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents">DDiscFormat2TrackAtOnceEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-canceladdtrack">IDiscFormat2TrackAtOnce::CancelAddTrack</a>
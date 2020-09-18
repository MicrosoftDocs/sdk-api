---
UID: NF:imapi2.DDiscFormat2EraseEvents.Update
title: DDiscFormat2EraseEvents::Update (imapi2.h)
description: Implement this method to receive progress notification of the current erase operation.
helpviewer_keywords: ["DDiscFormat2EraseEvents interface [IMAPI]","Update method","DDiscFormat2EraseEvents.Update","DDiscFormat2EraseEvents::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DDiscFormat2EraseEvents interface","imapi.ddiscformat2eraseevents_update","imapi2/DDiscFormat2EraseEvents::Update"]
old-location: imapi\ddiscformat2eraseevents_update.htm
tech.root: imapi
ms.assetid: 9cb52a79-84cf-49e5-a6b8-7baacb403ce9
ms.date: 12/05/2018
ms.keywords: DDiscFormat2EraseEvents interface [IMAPI],Update method, DDiscFormat2EraseEvents.Update, DDiscFormat2EraseEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2EraseEvents interface, imapi.ddiscformat2eraseevents_update, imapi2/DDiscFormat2EraseEvents::Update
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
 - DDiscFormat2EraseEvents::Update
 - imapi2/DDiscFormat2EraseEvents::Update
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
 - DDiscFormat2EraseEvents.Update
---

# DDiscFormat2EraseEvents::Update


## -description

Implement this method to receive progress notification of the current erase operation.

## -parameters

### -param object [in]

The <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a> interface that initiated the erase operation. 

This parameter is a <b>MsftDiscFormat2Erase</b> object in script.

### -param elapsedSeconds [in]

Elapsed time, in seconds, of the erase operation.

### -param estimatedTotalSeconds [in]

Estimated time, in seconds, to complete the erase operation.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-erasemedia">IDiscFormat2Erase::EraseMedia</a> method. 

Notification is sent every 0.5 or 1.0 seconds depending on the method required to blank the media.

Total time estimates for a single erasure can vary as the operation progresses. The drive provides updated information that can affect the projected duration of the erasure.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents">DDiscFormat2EraseEvents</a>
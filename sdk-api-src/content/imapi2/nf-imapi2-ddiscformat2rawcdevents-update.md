---
UID: NF:imapi2.DDiscFormat2RawCDEvents.Update
title: DDiscFormat2RawCDEvents::Update (imapi2.h)
description: Implement this method to receive progress notification of the current raw-image write operation.
helpviewer_keywords: ["DDiscFormat2RawCDEvents interface [IMAPI]","Update method","DDiscFormat2RawCDEvents.Update","DDiscFormat2RawCDEvents::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DDiscFormat2RawCDEvents interface","imapi.ddiscformat2rawcdevents_update","imapi2/DDiscFormat2RawCDEvents::Update"]
old-location: imapi\ddiscformat2rawcdevents_update.htm
tech.root: imapi
ms.assetid: abe35eee-63a4-4109-8927-825f86b6e302
ms.date: 12/05/2018
ms.keywords: DDiscFormat2RawCDEvents interface [IMAPI],Update method, DDiscFormat2RawCDEvents.Update, DDiscFormat2RawCDEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2RawCDEvents interface, imapi.ddiscformat2rawcdevents_update, imapi2/DDiscFormat2RawCDEvents::Update
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
 - DDiscFormat2RawCDEvents::Update
 - imapi2/DDiscFormat2RawCDEvents::Update
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
 - DDiscFormat2RawCDEvents.Update
---

# DDiscFormat2RawCDEvents::Update


## -description

Implement this method to receive progress notification of the current raw-image write operation.

## -parameters

### -param object [in]

The <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2RawCD</b> object in script.

### -param progress [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs">IDiscFormat2RawCDEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2RawCD</b> object in script.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia">IDiscFormat2RawCD::WriteMedia</a> or <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia2">IDiscFormat2RawCD::WriteMedia2</a> method.

To stop the write process, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-cancelwrite">IDiscFormat2RawCD::CancelWrite</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents">DDiscFormat2RawCDEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-cancelwrite">IDiscFormat2RawCD::CancelWrite</a>
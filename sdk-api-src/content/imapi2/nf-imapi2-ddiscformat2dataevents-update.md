---
UID: NF:imapi2.DDiscFormat2DataEvents.Update
title: DDiscFormat2DataEvents::Update (imapi2.h)
description: Implement this method to receive progress notification of the current write operation. (DDiscFormat2DataEvents.Update)
helpviewer_keywords: ["DDiscFormat2DataEvents interface [IMAPI]","Update method","DDiscFormat2DataEvents.Update","DDiscFormat2DataEvents::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DDiscFormat2DataEvents interface","imapi.ddiscformat2dataevents_update","imapi2/DDiscFormat2DataEvents::Update"]
old-location: imapi\ddiscformat2dataevents_update.htm
tech.root: imapi
ms.assetid: 786fc936-9493-4cc3-a937-4d1f4b54fe88
ms.date: 12/05/2018
ms.keywords: DDiscFormat2DataEvents interface [IMAPI],Update method, DDiscFormat2DataEvents.Update, DDiscFormat2DataEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2DataEvents interface, imapi.ddiscformat2dataevents_update, imapi2/DDiscFormat2DataEvents::Update
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
 - DDiscFormat2DataEvents::Update
 - imapi2/DDiscFormat2DataEvents::Update
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
 - DDiscFormat2DataEvents.Update
---

# DDiscFormat2DataEvents::Update


## -description

Implement this method to receive progress notification of the current write operation.

## -parameters

### -param object [in]

The <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2Data</b> object in script.

### -param progress [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs">IDiscFormat2DataEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2Data</b> object in script.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write">IDiscFormat2Data::Write</a> method.

Notification is sent when the current action changes:

<ul>
<li>Once when initializing the hardware</li>
<li>Once when calibrating the power</li>
<li>Once when formatting the media, if required by the media type</li>
<li>Every 0.5 seconds during the write operation</li>
<li>Once after the operation completes</li>
</ul>
To stop the write process, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-cancelwrite">IDiscFormat2Data::CancelWrite</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>

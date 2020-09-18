---
UID: NF:imapi.IDiscMasterProgressEvents.QueryCancel
title: IDiscMasterProgressEvents::QueryCancel (imapi.h)
description: Checks whether an AddData, AddAudioTrackBlocks, or RecordDisc operation should be canceled.
helpviewer_keywords: ["IDiscMasterProgressEvents interface [IMAPI]","QueryCancel method","IDiscMasterProgressEvents.QueryCancel","IDiscMasterProgressEvents::QueryCancel","QueryCancel","QueryCancel method [IMAPI]","QueryCancel method [IMAPI]","IDiscMasterProgressEvents interface","_win32_idiscmasterprogressevents_querycancel","base.idiscmasterprogressevents_querycancel","imapi.idiscmasterprogressevents_querycancel","imapi/IDiscMasterProgressEvents::QueryCancel"]
old-location: imapi\idiscmasterprogressevents_querycancel.htm
tech.root: imapi
ms.assetid: ca7ad8cb-0792-41ec-be5b-147be6750442
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],QueryCancel method, IDiscMasterProgressEvents.QueryCancel, IDiscMasterProgressEvents::QueryCancel, QueryCancel, QueryCancel method [IMAPI], QueryCancel method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_querycancel, base.idiscmasterprogressevents_querycancel, imapi.idiscmasterprogressevents_querycancel, imapi/IDiscMasterProgressEvents::QueryCancel
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMasterProgressEvents::QueryCancel
 - imapi/IDiscMasterProgressEvents::QueryCancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMasterProgressEvents.QueryCancel
---

# IDiscMasterProgressEvents::QueryCancel


## -description

Checks whether an 
<a href="/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-adddata">AddData</a>, 
<a href="/windows/desktop/api/imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks">AddAudioTrackBlocks</a>, or 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> operation should be canceled.

## -parameters

### -param pbCancel [out]

If this parameter is <b>TRUE</b>, cancel the burn. If this parameter is <b>FALSE</b>, continue the burn.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>
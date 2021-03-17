---
UID: NF:imapi.IDiscMaster.RecordDisc
title: IDiscMaster::RecordDisc (imapi.h)
description: Burns the staged image to media in the active disc recorder.
helpviewer_keywords: ["IDiscMaster interface [IMAPI]","RecordDisc method","IDiscMaster.RecordDisc","IDiscMaster::RecordDisc","RecordDisc","RecordDisc method [IMAPI]","RecordDisc method [IMAPI]","IDiscMaster interface","_win32_idiscmaster_recorddisc","base.idiscmaster_recorddisc","imapi.idiscmaster_recorddisc","imapi/IDiscMaster::RecordDisc"]
old-location: imapi\idiscmaster_recorddisc.htm
tech.root: imapi
ms.assetid: 2b234dc5-2409-49d8-83be-0ffea74f5bcf
ms.date: 12/05/2018
ms.keywords: IDiscMaster interface [IMAPI],RecordDisc method, IDiscMaster.RecordDisc, IDiscMaster::RecordDisc, RecordDisc, RecordDisc method [IMAPI], RecordDisc method [IMAPI],IDiscMaster interface, _win32_idiscmaster_recorddisc, base.idiscmaster_recorddisc, imapi.idiscmaster_recorddisc, imapi/IDiscMaster::RecordDisc
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
 - IDiscMaster::RecordDisc
 - imapi/IDiscMaster::RecordDisc
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
 - IDiscMaster.RecordDisc
---

# IDiscMaster::RecordDisc


## -description

Burns the staged image to media in the active disc recorder.

## -parameters

### -param bSimulate [in]

Indicates whether the media is burned. If this parameter is <b>TRUE</b>, media in the active disc recorder is not actually burned. Instead, a simulated burn is performed. The simulation is a good test of a disc recorder, because most of the operations are performed as in a real burn. If this parameter is <b>FALSE</b>, then the media in the recorder is actually burned.

### -param bEjectAfterBurn [in]

Indicates whether to eject the media after the burn. If this parameter is <b>TRUE</b>, the media is ejected. If this parameter is <b>FALSE</b>, the media is not ejected.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

This method returns when the burn is complete, although progress callbacks are made if registered with the 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressadvise">ProgressAdvise</a> method. Any errors cause this method to return, with little or no corrective action on the part of this method. 

The staged image data is not valid after a call to 
<b>RecordDisc</b>. This allows the application to perform either a simulated or actual burn of the media. For security, the contents of the stash file are cleared automatically after successful completion of the first call to this method. A disc must be restaged to burn it again.

The 
<b>RecordDisc</b> method expects to work with blank media for audio. Otherwise, the media may need to be erased (for example, CD-RW media in a CD-RW drive). See 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-erase">IDiscRecorder::Erase</a>.

The 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a> method determines if there is an IMAPI multi-session disc in the active drive upon setting. If so, IMAPI goes into multi-session mode automatically. If in multi-session mode and a call is made to 
<b>RecordDisc</b>, the same disc that established multi-session mode must be in the active recorder or an error code of IMAPI_E_WRONGDISC will be returned.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>
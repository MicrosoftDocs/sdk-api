---
UID: NF:imapi.IDiscMaster.SetActiveDiscRecorder
title: IDiscMaster::SetActiveDiscRecorder (imapi.h)
description: Selects an active disc recorder. The active disc recorder is the recorder where a burn will occur when RecordDisc is called.
helpviewer_keywords: ["IDiscMaster interface [IMAPI]","SetActiveDiscRecorder method","IDiscMaster.SetActiveDiscRecorder","IDiscMaster::SetActiveDiscRecorder","SetActiveDiscRecorder","SetActiveDiscRecorder method [IMAPI]","SetActiveDiscRecorder method [IMAPI]","IDiscMaster interface","_win32_idiscmaster_setactivediscrecorder","base.idiscmaster_setactivediscrecorder","imapi.idiscmaster_setactivediscrecorder","imapi/IDiscMaster::SetActiveDiscRecorder"]
old-location: imapi\idiscmaster_setactivediscrecorder.htm
tech.root: imapi
ms.assetid: 5f2e9135-d251-4702-b5d1-51d9b445a4f5
ms.date: 12/05/2018
ms.keywords: IDiscMaster interface [IMAPI],SetActiveDiscRecorder method, IDiscMaster.SetActiveDiscRecorder, IDiscMaster::SetActiveDiscRecorder, SetActiveDiscRecorder, SetActiveDiscRecorder method [IMAPI], SetActiveDiscRecorder method [IMAPI],IDiscMaster interface, _win32_idiscmaster_setactivediscrecorder, base.idiscmaster_setactivediscrecorder, imapi.idiscmaster_setactivediscrecorder, imapi/IDiscMaster::SetActiveDiscRecorder
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
 - IDiscMaster::SetActiveDiscRecorder
 - imapi/IDiscMaster::SetActiveDiscRecorder
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
 - IDiscMaster.SetActiveDiscRecorder
---

# IDiscMaster::SetActiveDiscRecorder


## -description

Selects an active disc recorder. The active disc recorder is the recorder where a burn will occur when 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> is called.

## -parameters

### -param pRecorder [in]

Pointer to the 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a> interface of a disc recorder object. This pointer should have been returned by a previous call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscrecorders">EnumDiscRecorders</a>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

<b>SetActiveDiscRecorder</b> must be called after the media to be used has been inserted, and before calling 
<a href="/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-adddata">IJolietDiscMaster::AddData</a>.

Selecting a recorder while in an active Joliet format will cause IMAPI to read information from the currently installed recorder disc. If this disc is a previous IMAPI Joliet disc and has space for another session, IMAPI automatically sets itself to multi-session mode. This disc must be in the active recorder when 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> is called.

The <b>MaxWriteSpeed</b> property is updated when this method is called. The default setting is the highest write speed.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>
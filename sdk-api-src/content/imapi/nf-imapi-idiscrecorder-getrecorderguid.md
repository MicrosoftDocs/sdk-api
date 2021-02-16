---
UID: NF:imapi.IDiscRecorder.GetRecorderGUID
title: IDiscRecorder::GetRecorderGUID (imapi.h)
description: Retrieves the GUID of the physical disc recorder currently associated with the recorder object.
helpviewer_keywords: ["GetRecorderGUID","GetRecorderGUID method [IMAPI]","GetRecorderGUID method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetRecorderGUID method","IDiscRecorder.GetRecorderGUID","IDiscRecorder::GetRecorderGUID","_win32_idiscrecorder_getrecorderguid","base.idiscrecorder_getrecorderguid","imapi.idiscrecorder_getrecorderguid","imapi/IDiscRecorder::GetRecorderGUID"]
old-location: imapi\idiscrecorder_getrecorderguid.htm
tech.root: imapi
ms.assetid: 9d13d352-bc48-43c7-9800-12855d754435
ms.date: 12/05/2018
ms.keywords: GetRecorderGUID, GetRecorderGUID method [IMAPI], GetRecorderGUID method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderGUID method, IDiscRecorder.GetRecorderGUID, IDiscRecorder::GetRecorderGUID, _win32_idiscrecorder_getrecorderguid, base.idiscrecorder_getrecorderguid, imapi.idiscrecorder_getrecorderguid, imapi/IDiscRecorder::GetRecorderGUID
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
 - IDiscRecorder::GetRecorderGUID
 - imapi/IDiscRecorder::GetRecorderGUID
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
 - IDiscRecorder.GetRecorderGUID
---

# IDiscRecorder::GetRecorderGUID


## -description

Retrieves the GUID of the physical disc recorder currently associated with the recorder object.

## -parameters

### -param pbyUniqueID [in]

Pointer to a GUID buffer to be filled in with this recorder's current GUID information. To query the required buffer size, use <b>NULL</b>.

### -param ulBufferSize [in]

Size of the GUID buffer. If <i>pbyUniqueID</i> is <b>NULL</b>, this parameter must be zero.

### -param pulReturnSizeRequired [out]

Size of the GUID information.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>
---
UID: NF:imapi2.IDiscFormat2Erase.put_Recorder
title: IDiscFormat2Erase::put_Recorder (imapi2.h)
description: Sets the recording device to use in the erase operation.
helpviewer_keywords: ["IDiscFormat2Erase interface [IMAPI]","put_Recorder method","IDiscFormat2Erase.put_Recorder","IDiscFormat2Erase::put_Recorder","imapi.idiscformat2erase_put_recorder","imapi2/IDiscFormat2Erase::put_Recorder","put_Recorder","put_Recorder method [IMAPI]","put_Recorder method [IMAPI]","IDiscFormat2Erase interface"]
old-location: imapi\idiscformat2erase_put_recorder.htm
tech.root: imapi
ms.assetid: d38c0d75-eb9c-4b8c-bf0e-7f05eb2f5116
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],put_Recorder method, IDiscFormat2Erase.put_Recorder, IDiscFormat2Erase::put_Recorder, imapi.idiscformat2erase_put_recorder, imapi2/IDiscFormat2Erase::put_Recorder, put_Recorder, put_Recorder method [IMAPI], put_Recorder method [IMAPI],IDiscFormat2Erase interface
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
 - IDiscFormat2Erase::put_Recorder
 - imapi2/IDiscFormat2Erase::put_Recorder
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
 - IDiscFormat2Erase.put_Recorder
---

# IDiscFormat2Erase::put_Recorder


## -description

Sets the recording device to use in the erase operation.

## -parameters

### -param value [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface that identifies the recording device to use in the erase operation.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

The recorder must be compatible with the format defined by this  interface. To determine compatibility, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-isrecordersupported">IDiscFormat2::IsRecorderSupported</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-get_recorder">IDiscFormat2Erase::get_Recorder</a>
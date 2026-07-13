---
UID: NF:imapi.IDiscRecorder.Eject
title: IDiscRecorder::Eject (imapi.h)
description: Unlocks and ejects the tray of the disc recorder, if possible.
helpviewer_keywords: ["Eject","Eject method [IMAPI]","Eject method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","Eject method","IDiscRecorder.Eject","IDiscRecorder::Eject","_win32_idiscrecorder_eject","base.idiscrecorder_eject","imapi.idiscrecorder_eject","imapi/IDiscRecorder::Eject"]
old-location: imapi\idiscrecorder_eject.htm
tech.root: imapi
ms.assetid: 29a40f49-1567-4198-b682-a0e314858baf
ms.date: 12/05/2018
ms.keywords: Eject, Eject method [IMAPI], Eject method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],Eject method, IDiscRecorder.Eject, IDiscRecorder::Eject, _win32_idiscrecorder_eject, base.idiscrecorder_eject, imapi.idiscrecorder_eject, imapi/IDiscRecorder::Eject
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
 - IDiscRecorder::Eject
 - imapi/IDiscRecorder::Eject
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
 - IDiscRecorder.Eject
---

# IDiscRecorder::Eject


## -description

Unlocks and ejects the tray of the disc recorder, if possible.



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

Not all recorders support calls to eject their media. However, this method attempts to eject media.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>

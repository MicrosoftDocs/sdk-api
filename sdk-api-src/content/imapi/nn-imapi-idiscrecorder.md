---
UID: NN:imapi.IDiscRecorder
title: IDiscRecorder (imapi.h)
description: The IDiscRecorder interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as MSDiscMasterObj maintains an active disc recorder.
helpviewer_keywords: ["IDiscRecorder","IDiscRecorder interface [IMAPI]","IDiscRecorder interface [IMAPI]","described","_win32_idiscrecorder","base.idiscrecorder","imapi.idiscrecorder","imapi/IDiscRecorder"]
old-location: imapi\idiscrecorder.htm
tech.root: imapi
ms.assetid: fc861cbb-a14e-499e-8b80-f5912e4f6076
ms.date: 12/05/2018
ms.keywords: IDiscRecorder, IDiscRecorder interface [IMAPI], IDiscRecorder interface [IMAPI],described, _win32_idiscrecorder, base.idiscrecorder, imapi.idiscrecorder, imapi/IDiscRecorder
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
 - IDiscRecorder
 - imapi/IDiscRecorder
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
 - IDiscRecorder
 - IDiscRecorder.Init
---

# IDiscRecorder interface


## -description

The 
<b>IDiscRecorder</b> interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as <b>MSDiscMasterObj</b> maintains an active disc recorder.

An 
<b>IDiscRecorder</b> object represents a single hardware device, but there can be multiple instances of 
<b>IDiscRecorder</b> all referencing the same hardware device. In this case, use 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-openexclusive">OpenExclusive</a> to access that device.

## -inheritance

The <b>IDiscRecorder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiscRecorder</b> also has these types of members:

## -remarks

All 
<b>IDiscRecorder</b> interfaces may be used on an 
<b>IDiscRecorder</b> object even if the disc recorder is not the active disc recorder. The IMAPI client does not have to call 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">IDiscMaster::SetActiveDiscRecorder</a> first.

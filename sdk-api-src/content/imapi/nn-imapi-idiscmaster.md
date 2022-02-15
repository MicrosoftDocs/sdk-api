---
UID: NN:imapi.IDiscMaster
title: IDiscMaster (imapi.h)
description: The IDiscMaster interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc.
helpviewer_keywords: ["IDiscMaster","IDiscMaster interface [IMAPI]","IDiscMaster interface [IMAPI]","described","_win32_idiscmaster","base.idiscmaster","imapi.idiscmaster","imapi/IDiscMaster"]
old-location: imapi\idiscmaster.htm
tech.root: imapi
ms.assetid: 1473e79e-a13a-4bc5-b80d-d8921fdc9952
ms.date: 12/05/2018
ms.keywords: IDiscMaster, IDiscMaster interface [IMAPI], IDiscMaster interface [IMAPI],described, _win32_idiscmaster, base.idiscmaster, imapi.idiscmaster, imapi/IDiscMaster
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
 - IDiscMaster
 - imapi/IDiscMaster
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
 - IDiscMaster
---

# IDiscMaster interface


## -description

The 
<b>IDiscMaster</b> interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc. Although an image mastering object can support several formats, it may not be possible to access all formats through a specific recorder. For this reason, you must select a recorder with 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a> after selecting a format with 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>.

## -inheritance

The <b>IDiscMaster</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiscMaster</b> also has these types of members:


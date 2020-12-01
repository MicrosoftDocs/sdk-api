---
UID: NF:imapi.IDiscMaster.ProgressAdvise
title: IDiscMaster::ProgressAdvise (imapi.h)
description: Registers an application for progress notifications.
helpviewer_keywords: ["IDiscMaster interface [IMAPI]","ProgressAdvise method","IDiscMaster.ProgressAdvise","IDiscMaster::ProgressAdvise","ProgressAdvise","ProgressAdvise method [IMAPI]","ProgressAdvise method [IMAPI]","IDiscMaster interface","_win32_idiscmaster_progressadvise","base.idiscmaster_progressadvise","imapi.idiscmaster_progressadvise","imapi/IDiscMaster::ProgressAdvise"]
old-location: imapi\idiscmaster_progressadvise.htm
tech.root: imapi
ms.assetid: 64966230-2042-46cb-9974-adbe382723a1
ms.date: 12/05/2018
ms.keywords: IDiscMaster interface [IMAPI],ProgressAdvise method, IDiscMaster.ProgressAdvise, IDiscMaster::ProgressAdvise, ProgressAdvise, ProgressAdvise method [IMAPI], ProgressAdvise method [IMAPI],IDiscMaster interface, _win32_idiscmaster_progressadvise, base.idiscmaster_progressadvise, imapi.idiscmaster_progressadvise, imapi/IDiscMaster::ProgressAdvise
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
 - IDiscMaster::ProgressAdvise
 - imapi/IDiscMaster::ProgressAdvise
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
 - IDiscMaster.ProgressAdvise
---

# IDiscMaster::ProgressAdvise


## -description

Registers an application for progress notifications.

## -parameters

### -param pEvents [in]

Pointer to an 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a> interface that receives the progress notifications.

### -param pvCookie [out]

Uniquely identifies this registration. Save this value because it will be needed by the 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressunadvise">ProgressUnadvise</a> method.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>
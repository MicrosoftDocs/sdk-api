---
UID: NF:imapi.IDiscMaster.ProgressUnadvise
title: IDiscMaster::ProgressUnadvise (imapi.h)
description: Cancels progress notifications for an application.
helpviewer_keywords: ["IDiscMaster interface [IMAPI]","ProgressUnadvise method","IDiscMaster.ProgressUnadvise","IDiscMaster::ProgressUnadvise","ProgressUnadvise","ProgressUnadvise method [IMAPI]","ProgressUnadvise method [IMAPI]","IDiscMaster interface","_win32_idiscmaster_progressunadvise","base.idiscmaster_progressunadvise","imapi.idiscmaster_progressunadvise","imapi/IDiscMaster::ProgressUnadvise"]
old-location: imapi\idiscmaster_progressunadvise.htm
tech.root: imapi
ms.assetid: b2729ff7-aefb-40cf-ae7b-9451fbe10bbb
ms.date: 12/05/2018
ms.keywords: IDiscMaster interface [IMAPI],ProgressUnadvise method, IDiscMaster.ProgressUnadvise, IDiscMaster::ProgressUnadvise, ProgressUnadvise, ProgressUnadvise method [IMAPI], ProgressUnadvise method [IMAPI],IDiscMaster interface, _win32_idiscmaster_progressunadvise, base.idiscmaster_progressunadvise, imapi.idiscmaster_progressunadvise, imapi/IDiscMaster::ProgressUnadvise
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
 - IDiscMaster::ProgressUnadvise
 - imapi/IDiscMaster::ProgressUnadvise
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
 - IDiscMaster.ProgressUnadvise
---

# IDiscMaster::ProgressUnadvise


## -description

Cancels progress notifications for an application.

## -parameters

### -param vCookie [in]

Value returned by a previous call to the 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressadvise">ProgressAdvise</a> method.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>
---
UID: NF:imapi.IDiscMaster.Close
title: IDiscMaster::Close (imapi.h)
description: Closes the interface so other applications can use it.
helpviewer_keywords: ["Close","Close method [IMAPI]","Close method [IMAPI]","IDiscMaster interface","IDiscMaster interface [IMAPI]","Close method","IDiscMaster.Close","IDiscMaster::Close","_win32_idiscmaster_close","base.idiscmaster_close","imapi.idiscmaster_close","imapi/IDiscMaster::Close"]
old-location: imapi\idiscmaster_close.htm
tech.root: imapi
ms.assetid: c5ebeca1-baaa-49ac-87ac-134d4b37e8c9
ms.date: 12/05/2018
ms.keywords: Close, Close method [IMAPI], Close method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],Close method, IDiscMaster.Close, IDiscMaster::Close, _win32_idiscmaster_close, base.idiscmaster_close, imapi.idiscmaster_close, imapi/IDiscMaster::Close
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
 - IDiscMaster::Close
 - imapi/IDiscMaster::Close
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
 - IDiscMaster.Close
---

# IDiscMaster::Close


## -description

Closes the interface so other applications can use it.



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

Content not committed to media through a call to 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a> is lost.

Closing an already closed interface returns S_OK.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>

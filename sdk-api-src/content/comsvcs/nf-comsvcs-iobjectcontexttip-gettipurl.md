---
UID: NF:comsvcs.IObjectContextTip.GetTipUrl
title: IObjectContextTip::GetTipUrl (comsvcs.h)
description: Retrieves the URL of the TIP context.
helpviewer_keywords: ["GetTipUrl","GetTipUrl method [COM+]","GetTipUrl method [COM+]","IObjectContextTip interface","IObjectContextTip interface [COM+]","GetTipUrl method","IObjectContextTip.GetTipUrl","IObjectContextTip::GetTipUrl","_cos_IObjectContextTip_GetTipUrl","comsvcs/IObjectContextTip::GetTipUrl","cos.iobjectcontexttip_gettipurl"]
old-location: cos\iobjectcontexttip_gettipurl.htm
tech.root: cos
ms.assetid: 9948a1b4-efbe-4a44-a67d-ea91a846708f
ms.date: 12/05/2018
ms.keywords: GetTipUrl, GetTipUrl method [COM+], GetTipUrl method [COM+],IObjectContextTip interface, IObjectContextTip interface [COM+],GetTipUrl method, IObjectContextTip.GetTipUrl, IObjectContextTip::GetTipUrl, _cos_IObjectContextTip_GetTipUrl, comsvcs/IObjectContextTip::GetTipUrl, cos.iobjectcontexttip_gettipurl
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IObjectContextTip::GetTipUrl
 - comsvcs/IObjectContextTip::GetTipUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectContextTip.GetTipUrl
---

# IObjectContextTip::GetTipUrl


## -description

Retrieves the URL of the TIP context.

## -parameters

### -param pTipUrl [out, retval]

The URL of the TIP transaction context, or <b>NULL</b> if the transaction context does not exist.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontexttip">IObjectContextTip</a>
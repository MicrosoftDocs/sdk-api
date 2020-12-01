---
UID: NF:xenroll.IEnroll2.SetHStoreMy
title: IEnroll2::SetHStoreMy (xenroll.h)
description: The SetHStoreMy method specifies the handle to use for the MY store. This method was first defined in the IEnroll2 interface.
helpviewer_keywords: ["IEnroll interface [Security]","SetHStoreMy method","IEnroll2 interface [Security]","SetHStoreMy method","IEnroll2.SetHStoreMy","IEnroll2::SetHStoreMy","IEnroll::SetHStoreMy","SetHStoreMy","SetHStoreMy method [Security]","SetHStoreMy method [Security]","IEnroll interface","SetHStoreMy method [Security]","IEnroll2 interface","security.ienroll4_sethstoremy","xenroll/IEnroll2::SetHStoreMy","xenroll/IEnroll::SetHStoreMy"]
old-location: security\ienroll4_sethstoremy.htm
tech.root: security
ms.assetid: 669c8fe4-def3-41c5-82fc-95c26f3950c8
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],SetHStoreMy method, IEnroll2 interface [Security],SetHStoreMy method, IEnroll2.SetHStoreMy, IEnroll2::SetHStoreMy, IEnroll::SetHStoreMy, SetHStoreMy, SetHStoreMy method [Security], SetHStoreMy method [Security],IEnroll interface, SetHStoreMy method [Security],IEnroll2 interface, security.ienroll4_sethstoremy, xenroll/IEnroll2::SetHStoreMy, xenroll/IEnroll::SetHStoreMy
req.header: xenroll.h
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
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll2::SetHStoreMy
 - xenroll/IEnroll2::SetHStoreMy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.SetHStoreMy
 - IEnroll2.SetHStoreMy
---

# IEnroll2::SetHStoreMy


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetHStoreMy</b> method specifies the handle to use for the MY store. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param hStore [in]

Certificate store handle to use for the MY store.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a>
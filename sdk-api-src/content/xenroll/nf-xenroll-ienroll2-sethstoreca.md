---
UID: NF:xenroll.IEnroll2.SetHStoreCA
title: IEnroll2::SetHStoreCA (xenroll.h)
description: The SetHStoreCA method specifies the handle to use for the CA store. This method was first defined in the IEnroll2 interface.
helpviewer_keywords: ["IEnroll2 interface [Security]","SetHStoreCA method","IEnroll2.SetHStoreCA","IEnroll2::SetHStoreCA","SetHStoreCA","SetHStoreCA method [Security]","SetHStoreCA method [Security]","IEnroll2 interface","security.ienroll4_sethstoreca","xenroll/IEnroll2::SetHStoreCA"]
old-location: security\ienroll4_sethstoreca.htm
tech.root: security
ms.assetid: d70fa8c0-7cdf-4023-9700-68f24d9116af
ms.date: 12/05/2018
ms.keywords: IEnroll2 interface [Security],SetHStoreCA method, IEnroll2.SetHStoreCA, IEnroll2::SetHStoreCA, SetHStoreCA, SetHStoreCA method [Security], SetHStoreCA method [Security],IEnroll2 interface, security.ienroll4_sethstoreca, xenroll/IEnroll2::SetHStoreCA
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
 - IEnroll2::SetHStoreCA
 - xenroll/IEnroll2::SetHStoreCA
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
 - IEnroll2.SetHStoreCA
---

# IEnroll2::SetHStoreCA


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetHStoreCA</b> method specifies the handle to use for the CA store. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param hStore [in]

Certificate store handle to use for the CA store.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>
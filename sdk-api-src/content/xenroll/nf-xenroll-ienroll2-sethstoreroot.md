---
UID: NF:xenroll.IEnroll2.SetHStoreROOT
title: IEnroll2::SetHStoreROOT (xenroll.h)
description: The SetHStoreROOT method specifies the handle to use for the Root store. This method was first defined in the IEnroll2 interface.
helpviewer_keywords: ["IEnroll2 interface [Security]","SetHStoreROOT method","IEnroll2.SetHStoreROOT","IEnroll2::SetHStoreROOT","SetHStoreROOT","SetHStoreROOT method [Security]","SetHStoreROOT method [Security]","IEnroll2 interface","security.ienroll4_sethstoreroot","xenroll/IEnroll2::SetHStoreROOT"]
old-location: security\ienroll4_sethstoreroot.htm
tech.root: security
ms.assetid: d41fabce-e0f8-4e82-b177-59a10af376ab
ms.date: 12/05/2018
ms.keywords: IEnroll2 interface [Security],SetHStoreROOT method, IEnroll2.SetHStoreROOT, IEnroll2::SetHStoreROOT, SetHStoreROOT, SetHStoreROOT method [Security], SetHStoreROOT method [Security],IEnroll2 interface, security.ienroll4_sethstoreroot, xenroll/IEnroll2::SetHStoreROOT
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
 - IEnroll2::SetHStoreROOT
 - xenroll/IEnroll2::SetHStoreROOT
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
 - IEnroll2.SetHStoreROOT
---

# IEnroll2::SetHStoreROOT


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetHStoreROOT</b> method specifies the handle to use for the Root store. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

## -parameters

### -param hStore [in]

Certificate store handle to use for the Root store.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>
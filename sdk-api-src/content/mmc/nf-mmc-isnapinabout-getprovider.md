---
UID: NF:mmc.ISnapinAbout.GetProvider
title: ISnapinAbout::GetProvider (mmc.h)
description: The ISnapinAbout::GetProvider method enables the console to obtain the snap-in provider name.
helpviewer_keywords: ["GetProvider","GetProvider method [MMC]","GetProvider method [MMC]","ISnapinAbout interface","ISnapinAbout interface [MMC]","GetProvider method","ISnapinAbout.GetProvider","ISnapinAbout::GetProvider","_slate_isnapinabout_getprovider","mmc.isnapinabout_getprovider","mmc/ISnapinAbout::GetProvider"]
old-location: mmc\isnapinabout_getprovider.htm
tech.root: mmc
ms.assetid: a1e0d99c-3485-4a24-aff0-7391ec5f8f6b
ms.date: 12/05/2018
ms.keywords: GetProvider, GetProvider method [MMC], GetProvider method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetProvider method, ISnapinAbout.GetProvider, ISnapinAbout::GetProvider, _slate_isnapinabout_getprovider, mmc.isnapinabout_getprovider, mmc/ISnapinAbout::GetProvider
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - ISnapinAbout::GetProvider
 - mmc/ISnapinAbout::GetProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinAbout.GetProvider
---

# ISnapinAbout::GetProvider


## -description

The <b>ISnapinAbout::GetProvider</b> method enables the console to obtain the snap-in provider name.

## -parameters

### -param lpName [out]

A pointer to the text of the snap-in provider name.

## -returns

This method can return one of these values.

## -remarks

Memory for out parameters must be allocated using the COM API function 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-isnapinabout">ISnapinAbout</a>
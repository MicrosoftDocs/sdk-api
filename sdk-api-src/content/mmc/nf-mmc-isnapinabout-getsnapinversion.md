---
UID: NF:mmc.ISnapinAbout.GetSnapinVersion
title: ISnapinAbout::GetSnapinVersion (mmc.h)
description: Enables the console to obtain the snap-in's version number.
helpviewer_keywords: ["GetSnapinVersion","GetSnapinVersion method [MMC]","GetSnapinVersion method [MMC]","ISnapinAbout interface","ISnapinAbout interface [MMC]","GetSnapinVersion method","ISnapinAbout.GetSnapinVersion","ISnapinAbout::GetSnapinVersion","_slate_isnapinabout_getsnapinversion","mmc.isnapinabout_getsnapinversion","mmc/ISnapinAbout::GetSnapinVersion"]
old-location: mmc\isnapinabout_getsnapinversion.htm
tech.root: mmc
ms.assetid: c933bb14-cf07-4eca-9a97-c833ed5f5438
ms.date: 12/05/2018
ms.keywords: GetSnapinVersion, GetSnapinVersion method [MMC], GetSnapinVersion method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinVersion method, ISnapinAbout.GetSnapinVersion, ISnapinAbout::GetSnapinVersion, _slate_isnapinabout_getsnapinversion, mmc.isnapinabout_getsnapinversion, mmc/ISnapinAbout::GetSnapinVersion
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
 - ISnapinAbout::GetSnapinVersion
 - mmc/ISnapinAbout::GetSnapinVersion
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
 - ISnapinAbout.GetSnapinVersion
---

# ISnapinAbout::GetSnapinVersion


## -description

The ISnapinAbout::GetSnapinVersion method enables the console to obtain the snap-in's version number.

## -parameters

### -param lpVersion [out]

A pointer to the text of the snap-in version number.

## -returns

This method can return one of these values.

## -remarks

Memory for out parameters must be allocated using the COM function 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-isnapinabout">ISnapinAbout</a>
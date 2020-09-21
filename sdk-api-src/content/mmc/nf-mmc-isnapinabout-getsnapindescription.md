---
UID: NF:mmc.ISnapinAbout.GetSnapinDescription
title: ISnapinAbout::GetSnapinDescription (mmc.h)
description: Enables the console to obtain the text for the snap-in's description box.
helpviewer_keywords: ["GetSnapinDescription","GetSnapinDescription method [MMC]","GetSnapinDescription method [MMC]","ISnapinAbout interface","ISnapinAbout interface [MMC]","GetSnapinDescription method","ISnapinAbout.GetSnapinDescription","ISnapinAbout::GetSnapinDescription","_slate_isnapinabout_getsnapindescription","mmc.isnapinabout_getsnapindescription","mmc/ISnapinAbout::GetSnapinDescription"]
old-location: mmc\isnapinabout_getsnapindescription.htm
tech.root: mmc
ms.assetid: 9f97d504-baba-4c9a-ab0b-ef585d2fe12c
ms.date: 12/05/2018
ms.keywords: GetSnapinDescription, GetSnapinDescription method [MMC], GetSnapinDescription method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinDescription method, ISnapinAbout.GetSnapinDescription, ISnapinAbout::GetSnapinDescription, _slate_isnapinabout_getsnapindescription, mmc.isnapinabout_getsnapindescription, mmc/ISnapinAbout::GetSnapinDescription
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
 - ISnapinAbout::GetSnapinDescription
 - mmc/ISnapinAbout::GetSnapinDescription
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
 - ISnapinAbout.GetSnapinDescription
---

# ISnapinAbout::GetSnapinDescription


## -description

The ISnapinAbout::GetSnapinDescription method enables the console to obtain the text for the snap-in's description box.

## -parameters

### -param lpDescription [out]

A pointer to the text for the description box on an <b>About</b> property page.

## -returns

This method can return one of these values.

## -remarks

The description should be limited to four lines of text to fit the description windows on the Snap-in Manager property pages.

Memory for out parameters must be allocated using the COM API function 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-isnapinabout">ISnapinAbout</a>
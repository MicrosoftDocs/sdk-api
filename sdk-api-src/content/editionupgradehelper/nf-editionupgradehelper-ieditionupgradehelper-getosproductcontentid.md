---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.GetOsProductContentId
title: IEditionUpgradeHelper::GetOsProductContentId (editionupgradehelper.h)
description: Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.
helpviewer_keywords: ["GetOsProductContentId","GetOsProductContentId method [Windows API]","GetOsProductContentId method [Windows API]","IEditionUpgradeHelper interface","IEditionUpgradeHelper interface [Windows API]","GetOsProductContentId method","IEditionUpgradeHelper.GetOsProductContentId","IEditionUpgradeHelper::GetOsProductContentId","editionupgradehelper/IEditionUpgradeHelper::GetOsProductContentId","winprog.ieditionupgradehelper_getosproductcontentid"]
old-location: winprog\ieditionupgradehelper_getosproductcontentid.htm
tech.root: winprog
ms.assetid: 79EEDFF2-FDF9-4BC9-968A-3543892AE870
ms.date: 12/05/2018
ms.keywords: GetOsProductContentId, GetOsProductContentId method [Windows API], GetOsProductContentId method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],GetOsProductContentId method, IEditionUpgradeHelper.GetOsProductContentId, IEditionUpgradeHelper::GetOsProductContentId, editionupgradehelper/IEditionUpgradeHelper::GetOsProductContentId, winprog.ieditionupgradehelper_getosproductcontentid
req.header: editionupgradehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Editionupgradehelper.idl
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
 - IEditionUpgradeHelper::GetOsProductContentId
 - editionupgradehelper/IEditionUpgradeHelper::GetOsProductContentId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - editionupgradehelper.h
api_name:
 - IEditionUpgradeHelper.GetOsProductContentId
---

# IEditionUpgradeHelper::GetOsProductContentId


## -description

Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.

## -parameters

### -param contentId [out]

The content identifier that corresponds to the current installation of the operating system.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/editionupgradehelper/nn-editionupgradehelper-ieditionupgradehelper">IEditionUpgradeHelper</a>



<a href="/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-updateoperatingsystem">UpdateOperatingSystem</a>
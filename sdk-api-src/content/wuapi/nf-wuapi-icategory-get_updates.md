---
UID: NF:wuapi.ICategory.get_Updates
title: ICategory::get_Updates (wuapi.h)
description: Gets an interface that contains a collection of updates that immediately belong to the category.
helpviewer_keywords: ["ICategory interface [Windows Update Agent]","Updates property","ICategory.Updates","ICategory.get_Updates","ICategory::Updates","ICategory::get_Updates","Updates property [Windows Update Agent]","Updates property [Windows Update Agent]","ICategory interface","get_Updates","wua.icategory_updates","wuapi/ICategory::Updates","wuapi/ICategory::get_Updates"]
old-location: wua\icategory_updates.htm
tech.root: wua
ms.assetid: f611b2df-c77f-4df0-8d7d-c8ed18f0222a
ms.date: 12/05/2018
ms.keywords: ICategory interface [Windows Update Agent],Updates property, ICategory.Updates, ICategory.get_Updates, ICategory::Updates, ICategory::get_Updates, Updates property [Windows Update Agent], Updates property [Windows Update Agent],ICategory interface, get_Updates, wua.icategory_updates, wuapi/ICategory::Updates, wuapi/ICategory::get_Updates
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICategory::get_Updates
 - wuapi/ICategory::get_Updates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ICategory.Updates
 - ICategory.get_Updates
---

# ICategory::get_Updates


## -description

Gets an interface that contains a collection of updates that immediately belong to the category.

This property is read-only.

## -parameters

## -remarks

The returned updates are applicable to the computer. They may or may not be installed on that computer.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a>
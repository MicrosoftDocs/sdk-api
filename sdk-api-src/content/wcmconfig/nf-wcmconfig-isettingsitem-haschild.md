---
UID: NF:wcmconfig.ISettingsItem.HasChild
title: ISettingsItem::HasChild (wcmconfig.h)
description: Determines whether the current item has a child item.
helpviewer_keywords: ["HasChild","HasChild method [SMI]","HasChild method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","HasChild method","ISettingsItem.HasChild","ISettingsItem::HasChild","smi.isettingsitem_haschild","wcmconfig/ISettingsItem::HasChild"]
old-location: smi\isettingsitem_haschild.htm
tech.root: SMI
ms.assetid: 6c22cb66-5116-4107-9fb0-a6a4161b6f8e
ms.date: 12/05/2018
ms.keywords: HasChild, HasChild method [SMI], HasChild method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],HasChild method, ISettingsItem.HasChild, ISettingsItem::HasChild, smi.isettingsitem_haschild, wcmconfig/ISettingsItem::HasChild
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsItem::HasChild
 - wcmconfig/ISettingsItem::HasChild
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem.HasChild
---

# ISettingsItem::HasChild


## -description

Determines  whether the current item has a child item.

## -parameters

### -param ItemHasChild [out]

<b>True</b> if a child item is present, <b>false</b> otherwise.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>
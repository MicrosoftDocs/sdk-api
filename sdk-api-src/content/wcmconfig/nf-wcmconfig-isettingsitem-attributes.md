---
UID: NF:wcmconfig.ISettingsItem.Attributes
title: ISettingsItem::Attributes (wcmconfig.h)
description: Gets the dictionary of attributes.
helpviewer_keywords: ["Attributes","Attributes method [SMI]","Attributes method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","Attributes method","ISettingsItem.Attributes","ISettingsItem::Attributes","smi.isettingsitem_attributes","wcmconfig/ISettingsItem::Attributes"]
old-location: smi\isettingsitem_attributes.htm
tech.root: SMI
ms.assetid: 7a6751f2-0934-4329-9ab2-9ae9802bc33e
ms.date: 12/05/2018
ms.keywords: Attributes, Attributes method [SMI], Attributes method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],Attributes method, ISettingsItem.Attributes, ISettingsItem::Attributes, smi.isettingsitem_attributes, wcmconfig/ISettingsItem::Attributes
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
 - ISettingsItem::Attributes
 - wcmconfig/ISettingsItem::Attributes
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
 - ISettingsItem.Attributes
---

# ISettingsItem::Attributes


## -description

Gets the dictionary of attributes.

## -parameters

### -param Attributes [out]

A pointer to an  <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> object that represents the dictionary of attributes.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate attributes.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>
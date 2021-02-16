---
UID: NF:wcmconfig.ISettingsItem.GetSettingType
title: ISettingsItem::GetSettingType (wcmconfig.h)
description: Gets the setting type for the item.
helpviewer_keywords: ["GetSettingType","GetSettingType method [SMI]","GetSettingType method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetSettingType method","ISettingsItem.GetSettingType","ISettingsItem::GetSettingType","smi.isettingsitem_getsettingtype","wcmconfig/ISettingsItem::GetSettingType"]
old-location: smi\isettingsitem_getsettingtype.htm
tech.root: SMI
ms.assetid: d222939f-9295-4751-8b32-586fa9930177
ms.date: 12/05/2018
ms.keywords: GetSettingType, GetSettingType method [SMI], GetSettingType method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetSettingType method, ISettingsItem.GetSettingType, ISettingsItem::GetSettingType, smi.isettingsitem_getsettingtype, wcmconfig/ISettingsItem::GetSettingType
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
 - ISettingsItem::GetSettingType
 - wcmconfig/ISettingsItem::GetSettingType
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
 - ISettingsItem.GetSettingType
---

# ISettingsItem::GetSettingType


## -description

Gets the setting type for the item.

## -parameters

### -param Type [out]

A <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmsettingtype">WcmSettingType</a> value that contains the setting type of the item.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>
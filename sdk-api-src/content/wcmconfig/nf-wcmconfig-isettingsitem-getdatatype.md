---
UID: NF:wcmconfig.ISettingsItem.GetDataType
title: ISettingsItem::GetDataType (wcmconfig.h)
description: Gets the type information for the item.
helpviewer_keywords: ["GetDataType","GetDataType method [SMI]","GetDataType method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetDataType method","ISettingsItem.GetDataType","ISettingsItem::GetDataType","smi.isettingsitem_getdatatype","wcmconfig/ISettingsItem::GetDataType"]
old-location: smi\isettingsitem_getdatatype.htm
tech.root: SMI
ms.assetid: 6ccb99aa-35d5-4f0b-a4f3-a42c4579bc4a
ms.date: 12/05/2018
ms.keywords: GetDataType, GetDataType method [SMI], GetDataType method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetDataType method, ISettingsItem.GetDataType, ISettingsItem::GetDataType, smi.isettingsitem_getdatatype, wcmconfig/ISettingsItem::GetDataType
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
 - ISettingsItem::GetDataType
 - wcmconfig/ISettingsItem::GetDataType
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
 - ISettingsItem.GetDataType
---

# ISettingsItem::GetDataType


## -description

Gets the type information for the item.

## -parameters

### -param Type [out]

A <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmdatatype">WcmDataType</a> value that indicates the data type of the item.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>
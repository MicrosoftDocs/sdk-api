---
UID: NF:wcmconfig.ISettingsItem.GetPath
title: ISettingsItem::GetPath (wcmconfig.h)
description: Gets the path for the item.
helpviewer_keywords: ["GetPath","GetPath method [SMI]","GetPath method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetPath method","ISettingsItem.GetPath","ISettingsItem::GetPath","smi.isettingsitem_getpath","wcmconfig/ISettingsItem::GetPath"]
old-location: smi\isettingsitem_getpath.htm
tech.root: SMI
ms.assetid: 221b5929-7300-4d01-b93e-7c82c446f52b
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [SMI], GetPath method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetPath method, ISettingsItem.GetPath, ISettingsItem::GetPath, smi.isettingsitem_getpath, wcmconfig/ISettingsItem::GetPath
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
 - ISettingsItem::GetPath
 - wcmconfig/ISettingsItem::GetPath
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
 - ISettingsItem.GetPath
---

# ISettingsItem::GetPath


## -description

Gets the path for the item.

## -parameters

### -param Path [out]

The path to the current setting. This path should be handled as opaque, and should be used only for invocations of <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-createsettingbypath">CreateSettingByPath</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getsettingbypath">GetSettingByPath</a>, or <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-removesettingbypath">RemoveSettingByPath</a>.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>
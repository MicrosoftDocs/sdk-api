---
UID: NF:wuapi.IUpdate.get_CanRequireSource
title: IUpdate::get_CanRequireSource (wuapi.h)
description: Gets a Boolean value that indicates whether the source media of the update is required for installation or uninstallation.
helpviewer_keywords: ["CanRequireSource property [Windows Update Agent]","CanRequireSource property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","CanRequireSource property","IUpdate.CanRequireSource","IUpdate.get_CanRequireSource","IUpdate::CanRequireSource","IUpdate::get_CanRequireSource","get_CanRequireSource","wua.iupdate_canrequiresource","wuapi/IUpdate::CanRequireSource","wuapi/IUpdate::get_CanRequireSource"]
old-location: wua\iupdate_canrequiresource.htm
tech.root: wua
ms.assetid: 45d1cdb1-6aab-4119-8cd5-a4217c9adc3e
ms.date: 12/05/2018
ms.keywords: CanRequireSource property [Windows Update Agent], CanRequireSource property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],CanRequireSource property, IUpdate.CanRequireSource, IUpdate.get_CanRequireSource, IUpdate::CanRequireSource, IUpdate::get_CanRequireSource, get_CanRequireSource, wua.iupdate_canrequiresource, wuapi/IUpdate::CanRequireSource, wuapi/IUpdate::get_CanRequireSource
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
 - IUpdate::get_CanRequireSource
 - wuapi/IUpdate::get_CanRequireSource
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
 - IUpdate.CanRequireSource
 - IUpdate.get_CanRequireSource
---

# IUpdate::get_CanRequireSource


## -description

Gets a Boolean value that indicates whether the source media of the update is required for installation or uninstallation.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the source media of the update is required for installation or uninstallation, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
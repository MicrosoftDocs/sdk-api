---
UID: NF:wuapi.IUpdate.get_IsUninstallable
title: IUpdate::get_IsUninstallable (wuapi.h)
description: Gets a Boolean value that indicates whether a user can uninstall the update from a computer.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","IsUninstallable property","IUpdate.IsUninstallable","IUpdate.get_IsUninstallable","IUpdate::IsUninstallable","IUpdate::get_IsUninstallable","IsUninstallable property [Windows Update Agent]","IsUninstallable property [Windows Update Agent]","IUpdate interface","get_IsUninstallable","wua.iupdate_isuninstallable","wuapi/IUpdate::IsUninstallable","wuapi/IUpdate::get_IsUninstallable"]
old-location: wua\iupdate_isuninstallable.htm
tech.root: wua
ms.assetid: 0f67461b-3df9-45e9-95b3-d7f46fa11162
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],IsUninstallable property, IUpdate.IsUninstallable, IUpdate.get_IsUninstallable, IUpdate::IsUninstallable, IUpdate::get_IsUninstallable, IsUninstallable property [Windows Update Agent], IsUninstallable property [Windows Update Agent],IUpdate interface, get_IsUninstallable, wua.iupdate_isuninstallable, wuapi/IUpdate::IsUninstallable, wuapi/IUpdate::get_IsUninstallable
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
 - IUpdate::get_IsUninstallable
 - wuapi/IUpdate::get_IsUninstallable
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
 - IUpdate.IsUninstallable
 - IUpdate.get_IsUninstallable
---

# IUpdate::get_IsUninstallable


## -description

Gets a Boolean value that indicates whether a user can uninstall the update from a computer.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update can be uninstalled, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
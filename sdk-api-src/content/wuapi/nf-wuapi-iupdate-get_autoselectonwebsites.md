---
UID: NF:wuapi.IUpdate.get_AutoSelectOnWebSites
title: IUpdate::get_AutoSelectOnWebSites (wuapi.h)
description: Gets a Boolean value that indicates whether the update is flagged to be automatically selected by Windows Update.
helpviewer_keywords: ["AutoSelectOnWebSites property [Windows Update Agent]","AutoSelectOnWebSites property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","AutoSelectOnWebSites property","IUpdate.AutoSelectOnWebSites","IUpdate.get_AutoSelectOnWebSites","IUpdate::AutoSelectOnWebSites","IUpdate::get_AutoSelectOnWebSites","get_AutoSelectOnWebSites","wua.iupdate_autoselectonwebsites","wuapi/IUpdate::AutoSelectOnWebSites","wuapi/IUpdate::get_AutoSelectOnWebSites"]
old-location: wua\iupdate_autoselectonwebsites.htm
tech.root: wua
ms.assetid: a27d7144-bd76-40e3-b8a7-951ae1974afb
ms.date: 12/05/2018
ms.keywords: AutoSelectOnWebSites property [Windows Update Agent], AutoSelectOnWebSites property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],AutoSelectOnWebSites property, IUpdate.AutoSelectOnWebSites, IUpdate.get_AutoSelectOnWebSites, IUpdate::AutoSelectOnWebSites, IUpdate::get_AutoSelectOnWebSites, get_AutoSelectOnWebSites, wua.iupdate_autoselectonwebsites, wuapi/IUpdate::AutoSelectOnWebSites, wuapi/IUpdate::get_AutoSelectOnWebSites
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
 - IUpdate::get_AutoSelectOnWebSites
 - wuapi/IUpdate::get_AutoSelectOnWebSites
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
 - IUpdate.AutoSelectOnWebSites
 - IUpdate.get_AutoSelectOnWebSites
---

# IUpdate::get_AutoSelectOnWebSites


## -description

Gets a Boolean value that indicates whether the update is flagged to be automatically selected by Windows Update.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update is flagged to be automatically selected by Windows Update, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
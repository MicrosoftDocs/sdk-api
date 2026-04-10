---
UID: NF:wuapi.IUpdate.get_IsInstalled
title: IUpdate::get_IsInstalled (wuapi.h)
description: Gets a Boolean value that indicates whether the update is installed on a computer when the search is performed.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","IsInstalled property","IUpdate.IsInstalled","IUpdate.get_IsInstalled","IUpdate::IsInstalled","IUpdate::get_IsInstalled","IsInstalled property [Windows Update Agent]","IsInstalled property [Windows Update Agent]","IUpdate interface","get_IsInstalled","wua.iupdate_isinstalled","wuapi/IUpdate::IsInstalled","wuapi/IUpdate::get_IsInstalled"]
old-location: wua\iupdate_isinstalled.htm
tech.root: wua
ms.assetid: 2adebe8e-554e-4337-9bbf-1d8967fefef1
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],IsInstalled property, IUpdate.IsInstalled, IUpdate.get_IsInstalled, IUpdate::IsInstalled, IUpdate::get_IsInstalled, IsInstalled property [Windows Update Agent], IsInstalled property [Windows Update Agent],IUpdate interface, get_IsInstalled, wua.iupdate_isinstalled, wuapi/IUpdate::IsInstalled, wuapi/IUpdate::get_IsInstalled
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
 - IUpdate::get_IsInstalled
 - wuapi/IUpdate::get_IsInstalled
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
 - IUpdate.IsInstalled
 - IUpdate.get_IsInstalled
---

# IUpdate::get_IsInstalled


## -description

Gets a Boolean value that indicates whether the update is installed on a computer when the search is performed.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update is installed, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
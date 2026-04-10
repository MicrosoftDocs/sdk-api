---
UID: NF:wuapi.IUpdate.get_IsMandatory
title: IUpdate::get_IsMandatory (wuapi.h)
description: Gets a Boolean value that indicates whether the installation of the update is mandatory.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","IsMandatory property","IUpdate.IsMandatory","IUpdate.get_IsMandatory","IUpdate::IsMandatory","IUpdate::get_IsMandatory","IsMandatory property [Windows Update Agent]","IsMandatory property [Windows Update Agent]","IUpdate interface","get_IsMandatory","wua.iupdate_ismandatory","wuapi/IUpdate::IsMandatory","wuapi/IUpdate::get_IsMandatory"]
old-location: wua\iupdate_ismandatory.htm
tech.root: wua
ms.assetid: 5052914f-7b92-4637-b188-dce4a8e15328
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],IsMandatory property, IUpdate.IsMandatory, IUpdate.get_IsMandatory, IUpdate::IsMandatory, IUpdate::get_IsMandatory, IsMandatory property [Windows Update Agent], IsMandatory property [Windows Update Agent],IUpdate interface, get_IsMandatory, wua.iupdate_ismandatory, wuapi/IUpdate::IsMandatory, wuapi/IUpdate::get_IsMandatory
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
 - IUpdate::get_IsMandatory
 - wuapi/IUpdate::get_IsMandatory
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
 - IUpdate.IsMandatory
 - IUpdate.get_IsMandatory
---

# IUpdate::get_IsMandatory


## -description

Gets a Boolean value that indicates whether the installation of the update is mandatory.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update is mandatory, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you try to mark a mandatory update as hidden, an error occurs.

Mandatory updates are updates to the Windows Update Agent (WUA) infrastructure. WUA may not require all mandatory updates to continue operating. However, these updates frequently improve performance or increase the number of products that WUA can offer.  We recommend that you install all mandatory updates.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
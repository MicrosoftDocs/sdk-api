---
UID: NF:wuapi.IUpdate.get_IsDownloaded
title: IUpdate::get_IsDownloaded (wuapi.h)
description: Gets a Boolean value that indicates whether all the update content is cached on the computer.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","IsDownloaded property","IUpdate.IsDownloaded","IUpdate.get_IsDownloaded","IUpdate::IsDownloaded","IUpdate::get_IsDownloaded","IsDownloaded property [Windows Update Agent]","IsDownloaded property [Windows Update Agent]","IUpdate interface","get_IsDownloaded","wua.iupdate_isdownloaded","wuapi/IUpdate::IsDownloaded","wuapi/IUpdate::get_IsDownloaded"]
old-location: wua\iupdate_isdownloaded.htm
tech.root: wua
ms.assetid: 4e20f2b0-096c-4ec6-b554-1891522b8933
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],IsDownloaded property, IUpdate.IsDownloaded, IUpdate.get_IsDownloaded, IUpdate::IsDownloaded, IUpdate::get_IsDownloaded, IsDownloaded property [Windows Update Agent], IsDownloaded property [Windows Update Agent],IUpdate interface, get_IsDownloaded, wua.iupdate_isdownloaded, wuapi/IUpdate::IsDownloaded, wuapi/IUpdate::get_IsDownloaded
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
 - IUpdate::get_IsDownloaded
 - wuapi/IUpdate::get_IsDownloaded
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
 - IUpdate.IsDownloaded
 - IUpdate.get_IsDownloaded
---

# IUpdate::get_IsDownloaded


## -description

Gets a Boolean value that indicates whether all the update content is cached on the computer.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update is downloaded, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>



<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloader">IUpdateDownloader</a>
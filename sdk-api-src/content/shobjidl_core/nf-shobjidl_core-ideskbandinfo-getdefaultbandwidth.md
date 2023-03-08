---
UID: NF:shobjidl_core.IDeskBandInfo.GetDefaultBandWidth
title: IDeskBandInfo::GetDefaultBandWidth (shobjidl_core.h)
description: Gets the band width that the bandsite initially uses to set the default width when the band is added.
helpviewer_keywords: ["DBIF_VIEWMODE_FLOATING","DBIF_VIEWMODE_NORMAL","DBIF_VIEWMODE_TRANSPARENT","DBIF_VIEWMODE_VERTICAL","GetDefaultBandWidth","GetDefaultBandWidth method [Windows Shell]","GetDefaultBandWidth method [Windows Shell]","IDeskBandInfo interface","IDeskBandInfo interface [Windows Shell]","GetDefaultBandWidth method","IDeskBandInfo.GetDefaultBandWidth","IDeskBandInfo::GetDefaultBandWidth","_shell_IDeskBandInfo_GetDefaultBandWidth","shell.IDeskBandInfo_GetDefaultBandWidth","shobjidl_core/IDeskBandInfo::GetDefaultBandWidth"]
old-location: shell\IDeskBandInfo_GetDefaultBandWidth.htm
tech.root: shell
ms.assetid: 2a900f9d-4727-4279-867d-ec4ed17cd374
ms.date: 12/05/2018
ms.keywords: DBIF_VIEWMODE_FLOATING, DBIF_VIEWMODE_NORMAL, DBIF_VIEWMODE_TRANSPARENT, DBIF_VIEWMODE_VERTICAL, GetDefaultBandWidth, GetDefaultBandWidth method [Windows Shell], GetDefaultBandWidth method [Windows Shell],IDeskBandInfo interface, IDeskBandInfo interface [Windows Shell],GetDefaultBandWidth method, IDeskBandInfo.GetDefaultBandWidth, IDeskBandInfo::GetDefaultBandWidth, _shell_IDeskBandInfo_GetDefaultBandWidth, shell.IDeskBandInfo_GetDefaultBandWidth, shobjidl_core/IDeskBandInfo::GetDefaultBandWidth
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBandInfo::GetDefaultBandWidth
 - shobjidl_core/IDeskBandInfo::GetDefaultBandWidth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDeskBandInfo.GetDefaultBandWidth
---

# IDeskBandInfo::GetDefaultBandWidth


## -description

<p class="CCE_Message">[<b>GetDefaultBandWidth</b> may be altered or unavailable in subsequent versions of the operating system or product.]

Gets the band width that the bandsite initially uses to set the default width when the band is added.

## -parameters

### -param dwBandID [in]

Type: <b>DWORD</b>

The band ID.

### -param dwViewMode [in]

Type: <b>DWORD</b>

The view mode of the band object. One of the following values: 



#### DBIF_VIEWMODE_NORMAL

The band object is being displayed in a horizontal band.



#### DBIF_VIEWMODE_VERTICAL

The band object is being displayed in a vertical band.



#### DBIF_VIEWMODE_FLOATING

The band object is being displayed in a floating band.



#### DBIF_VIEWMODE_TRANSPARENT

The band object is being displayed in a transparent band.

### -param pnWidth [out]

Type: <b>int*</b>

A pointer to the band width.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


---
UID: NF:shobjidl_core.IDeskBand.GetBandInfo
title: IDeskBand::GetBandInfo (shobjidl_core.h)
description: Gets state information for a band object.
helpviewer_keywords: ["DBIF_VIEWMODE_FLOATING","DBIF_VIEWMODE_NORMAL","DBIF_VIEWMODE_TRANSPARENT","DBIF_VIEWMODE_VERTICAL","GetBandInfo","GetBandInfo method [Windows Shell]","GetBandInfo method [Windows Shell]","IDeskBand interface","IDeskBand interface [Windows Shell]","GetBandInfo method","IDeskBand.GetBandInfo","IDeskBand::GetBandInfo","_win32_IDeskBand_GetBandInfo","shell.IDeskBand_GetBandInfo","shobjidl_core/IDeskBand::GetBandInfo"]
old-location: shell\IDeskBand_GetBandInfo.htm
tech.root: shell
ms.assetid: 7567a2f8-989e-4d11-ae55-209e4cfacad0
ms.date: 12/05/2018
ms.keywords: DBIF_VIEWMODE_FLOATING, DBIF_VIEWMODE_NORMAL, DBIF_VIEWMODE_TRANSPARENT, DBIF_VIEWMODE_VERTICAL, GetBandInfo, GetBandInfo method [Windows Shell], GetBandInfo method [Windows Shell],IDeskBand interface, IDeskBand interface [Windows Shell],GetBandInfo method, IDeskBand.GetBandInfo, IDeskBand::GetBandInfo, _win32_IDeskBand_GetBandInfo, shell.IDeskBand_GetBandInfo, shobjidl_core/IDeskBand::GetBandInfo
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBand::GetBandInfo
 - shobjidl_core/IDeskBand::GetBandInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBand.GetBandInfo
---

# IDeskBand::GetBandInfo


## -description

Gets state information for a band object.
<div class="alert"><b>Important</b>  You should use <a href="/windows/desktop/shell/taskbar-extensions">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters

### -param dwBandID

Type: <b>DWORD</b>

The identifier of the band, assigned by the container. The band object can retain this value if it is required.

### -param dwViewMode

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

### -param pdbi

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo">DESKBANDINFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo">DESKBANDINFO</a> structure that receives the band information for the object. The <b>dwMask</b> member of this structure indicates the specific information that is being requested.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
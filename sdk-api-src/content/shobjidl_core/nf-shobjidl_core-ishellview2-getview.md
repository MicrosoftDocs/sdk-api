---
UID: NF:shobjidl_core.IShellView2.GetView
title: IShellView2::GetView (shobjidl_core.h)
description: Requests the current or default Shell view, together with all other valid view identifiers (VIDs) supported by this implementation of IShellView2.
helpviewer_keywords: ["GetView","GetView method [Windows Shell]","GetView method [Windows Shell]","IShellView2 interface","IShellView2 interface [Windows Shell]","GetView method","IShellView2.GetView","IShellView2::GetView","SV2GV_CURRENTVIEW","SV2GV_DEFAULTVIEW","VID_Details","VID_LargeIcons","VID_List","VID_SmallIcons","VID_Tile","_win32_IShellView2_GetView","shell.IShellView2_GetView","shobjidl_core/IShellView2::GetView"]
old-location: shell\IShellView2_GetView.htm
tech.root: shell
ms.assetid: 74fe42fe-33de-483a-88e4-50da9c1f77c2
ms.date: 12/05/2018
ms.keywords: GetView, GetView method [Windows Shell], GetView method [Windows Shell],IShellView2 interface, IShellView2 interface [Windows Shell],GetView method, IShellView2.GetView, IShellView2::GetView, SV2GV_CURRENTVIEW, SV2GV_DEFAULTVIEW, VID_Details, VID_LargeIcons, VID_List, VID_SmallIcons, VID_Tile, _win32_IShellView2_GetView, shell.IShellView2_GetView, shobjidl_core/IShellView2::GetView
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView2::GetView
 - shobjidl_core/IShellView2::GetView
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
 - IShellView2.GetView
---

# IShellView2::GetView


## -description

Requests the current or default Shell view, together with all other valid view identifiers (VIDs) supported by this implementation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2">IShellView2</a>.

## -parameters

### -param pvid [out]

Type: <b>SHELLVIEWID*</b>

A pointer to the GUID of the requested view. The following views are defined in Shlguid.h.



#### VID_LargeIcons

{0057D0E0-3573-11CF-AE69-08002B2E1262}



#### VID_SmallIcons

{089000C0-3573-11CF-AE69-08002B2E1262}



#### VID_List

{0E1FA5E0-3573-11CF-AE69-08002B2E1262}



#### VID_Details

{137E7700-3573-11CF-AE69-08002B2E1262}



#### VID_Tile

{65F125E5-7BE1-4810-BA9D-D271C8432CE3}

### -param uView [in]

Type: <b>ULONG</b>

The type of view requested.



#### SV2GV_CURRENTVIEW

Current Shell view.



#### SV2GV_DEFAULTVIEW

Default Shell view.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a standard COM error code otherwise.

## -remarks

<b>IShellView2::GetView</b> retrieves a "viewset", which is the requested view (default or current) together with all other valid views for this instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2">IShellView2</a>. Calling <b>IShellView2::GetView</b> with the <b>SV2GV_CURRENTVIEW</b> returns a GUID representing the current view and also iterates through the valid VIDs. This information is stored for later use in validating a new view before it is displayed.

The view can also be affected by other factors. A global user default VID and <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">view mode</a> is set  when the user presses the <b>Apply to All Folders</b> button in the <b>Folder Options</b> window. The VID is determined from <b>IShellView2::GetView</b> with the <b>SV2GV_CURRENTVIEW</b> flag
and  the view mode is determined from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo">GetCurrentInfo</a>. The view can also be affected by the persisted folder default. Windows Explorer saves the VID and view mode of a folder if the user has previously visited it. In some cases, the folder you are navigating from also can influence the view mode created for the new view that you are entering.

The priority of these assorted views can be generally said to be the following:

<ol>
<li>Persisted folder default</li>
<li>Global user default</li>
<li>Default view (SV2GV_DEFAULTVIEW)</li>
<li>Previous view</li>
</ol>
The priority of the previous view can be higher if the <b>Remember each folder's view settings</b> option is not selected in <b>Folder Options</b>. Other factors such as policies can also come into play, so the list above should be viewed only as a very broad guideline.
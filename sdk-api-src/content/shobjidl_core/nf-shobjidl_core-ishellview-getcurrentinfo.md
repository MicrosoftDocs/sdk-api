---
UID: NF:shobjidl_core.IShellView.GetCurrentInfo
title: IShellView::GetCurrentInfo (shobjidl_core.h)
description: Gets the current folder settings.
helpviewer_keywords: ["GetCurrentInfo","GetCurrentInfo method [Windows Shell]","GetCurrentInfo method [Windows Shell]","IShellView interface","IShellView interface [Windows Shell]","GetCurrentInfo method","IShellView.GetCurrentInfo","IShellView::GetCurrentInfo","_win32_IShellView_GetCurrentInfo","shell.IShellView_GetCurrentInfo","shobjidl_core/IShellView::GetCurrentInfo"]
old-location: shell\IShellView_GetCurrentInfo.htm
tech.root: shell
ms.assetid: 69d18b4f-3a68-420c-a184-05c2f69a5ec6
ms.date: 12/05/2018
ms.keywords: GetCurrentInfo, GetCurrentInfo method [Windows Shell], GetCurrentInfo method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],GetCurrentInfo method, IShellView.GetCurrentInfo, IShellView::GetCurrentInfo, _win32_IShellView_GetCurrentInfo, shell.IShellView_GetCurrentInfo, shobjidl_core/IShellView::GetCurrentInfo
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView::GetCurrentInfo
 - shobjidl_core/IShellView::GetCurrentInfo
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
 - IShellView.GetCurrentInfo
---

# IShellView::GetCurrentInfo


## -description

Gets the current folder settings.

## -parameters

### -param pfs

Type: <b>LPFOLDERSETTINGS</b>

The address of a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure to receive the settings.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -remarks

Windows Explorer uses this method to query the view for standard settings.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
This method is used to retrieve the current view settings of the view.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Return as many of the settings as apply. This is intended to maintain the same basic settings when the user browses from view to view. For example, if the user sets the Details view, that view should be maintained as the user goes from one folder to the other in Windows Explorer mode.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
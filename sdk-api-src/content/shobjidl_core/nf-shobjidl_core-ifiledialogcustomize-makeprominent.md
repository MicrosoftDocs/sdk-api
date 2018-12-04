---
UID: NF:shobjidl_core.IFileDialogCustomize.MakeProminent
title: IFileDialogCustomize::MakeProminent
author: windows-sdk-content
description: Places a control in the dialog so that it stands out compared to other added controls.
old-location: shell\IFileDialogCustomize_MakeProminent.htm
tech.root: shell
ms.assetid: 7e7b1573-cbd7-49eb-a26d-e2aba0bb4495
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],MakeProminent method, IFileDialogCustomize.MakeProminent, IFileDialogCustomize::MakeProminent, MakeProminent, MakeProminent method [Windows Shell], MakeProminent method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_MakeProminent, shell_IFileDialogCustomize_MakeProminent, shobjidl_core/IFileDialogCustomize::MakeProminent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.MakeProminent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogCustomize::MakeProminent


## -description


Places a control in the dialog so that it stands out compared to other added controls.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method causes the control to be placed near the <b>Open</b> or <b>Save</b> button instead of being grouped with the rest of the custom controls.

Only check buttons (check boxes), push buttons, combo boxes, and menus—or a visual group that contains only a single item of one of those types—can be made prominent.

Only one control can be marked in this way. If a dialog has only one added control, that control is marked as prominent by default.




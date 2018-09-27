---
UID: NF:shobjidl_core.IFileDialogCustomize.StartVisualGroup
title: IFileDialogCustomize::StartVisualGroup
author: windows-sdk-content
description: Declares a visual group in the dialog. Subsequent calls to any &#0034;add&#0034; method add those elements to this group.
old-location: shell\IFileDialogCustomize_StartVisualGroup.htm
tech.root: shell
ms.assetid: 2626c820-3731-474d-9ddb-d2a8966c3d35
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],StartVisualGroup method, IFileDialogCustomize.StartVisualGroup, IFileDialogCustomize::StartVisualGroup, StartVisualGroup, StartVisualGroup method [Windows Shell], StartVisualGroup method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_StartVisualGroup, shell_IFileDialogCustomize_StartVisualGroup, shobjidl_core/IFileDialogCustomize::StartVisualGroup
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
 - IFileDialogCustomize.StartVisualGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogCustomize::StartVisualGroup


## -description


Declares a visual group in the dialog. Subsequent calls to any "add" method add those elements to this group.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the visual group.
                


### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains text, as a null-terminated Unicode string, that appears next to the visual group.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Controls will continue to be added to this visual group until you call <a href="https://msdn.microsoft.com/84aef9e1-2b70-4e8b-b261-cc49f8e65ead">IFileDialogCustomize::EndVisualGroup</a>.
              

A visual group can be hidden and disabled like any other control, except that doing so affects all of the controls within it. Individual members of the visual group can also be hidden and disabled singly.




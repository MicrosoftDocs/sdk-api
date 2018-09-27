---
UID: NF:shlobj_core.IShellFolderView.SetPoints
title: IShellFolderView::SetPoints
author: windows-sdk-content
description: SetPoints may be altered or unavailable.
old-location: shell\IShellFolderView_SetPoints.htm
tech.root: shell
ms.assetid: a226139a-c2b0-44d5-a0c3-790e27ab3a0f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IShellFolderView interface [Windows Shell],SetPoints method, IShellFolderView.SetPoints, IShellFolderView::SetPoints, SetPoints, SetPoints method [Windows Shell], SetPoints method [Windows Shell],IShellFolderView interface, _shell_IShellFolderView_SetPoints, shell.IShellFolderView_SetPoints, shlobj_core/IShellFolderView::SetPoints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IShellFolderView.SetPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::SetPoints


## -description


<p class="CCE_Message">[<b>SetPoints</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Copies the points at which the current selection is located into a data object.


## -parameters




### -param pDataObject [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the data object. This data object contains the points of location of the current selection. These points are given in coordinates relative to the ListView control that the view contains. These points can be used for positioning the object at the end of a drag-and-drop operation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This call is not needed if the drag-and-drop operation was originated by <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>.




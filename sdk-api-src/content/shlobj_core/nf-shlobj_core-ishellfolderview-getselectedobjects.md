---
UID: NF:shlobj_core.IShellFolderView.GetSelectedObjects
title: IShellFolderView::GetSelectedObjects
author: windows-sdk-content
description: Gets an array of the objects in the view that are selected and the number of those objects.
old-location: shell\IShellFolderView_GetSelectedObjects.htm
tech.root: shell
ms.assetid: 9cb41312-a401-4d24-a7a7-7b03478cf684
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSelectedObjects, GetSelectedObjects method [Windows Shell], GetSelectedObjects method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetSelectedObjects method, IShellFolderView.GetSelectedObjects, IShellFolderView::GetSelectedObjects, _shell_IShellFolderView_GetSelectedObjects, shell.IShellFolderView_GetSelectedObjects, shlobj_core/IShellFolderView::GetSelectedObjects
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
 - shlobj_core.h
api_name:
 - IShellFolderView.GetSelectedObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::GetSelectedObjects


## -description


<p class="CCE_Message">[This method has been deprecated. Use <a href="https://msdn.microsoft.com/d8ff0c8f-9678-455b-b7ec-9b651df769bc">IFolderView2::GetSelection</a> instead.]

Gets an array of the objects in the view that are selected and the number of those objects.


## -parameters




### -param pppidl [out]

Type: <b>PCUITEMID_CHILD**</b>

The address of a pointer that, when this method returns successfully, points to an array of the currently selected items in the view. The calling application is expected to free the array at <i>pppidl</i> using <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>. The calling application must not free the individual items contained in the array.


### -param puItems [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the number of items in the <i>pppidl</i> array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method provides constant pointers to internal data structures. The calling application is expected to act on them immediately and not cache them.




---
UID: NF:shobjidl_core.IFolderView.SelectAndPositionItems
title: IFolderView::SelectAndPositionItems
author: windows-sdk-content
description: Allows the selection and positioning of items visible in the folder's view.
old-location: shell\IFolderView_SelectAndPositionItems.htm
tech.root: shell
ms.assetid: 1263bba8-63c8-4630-ab59-bb4ae10061fc
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IFolderView interface [Windows Shell],SelectAndPositionItems method, IFolderView.SelectAndPositionItems, IFolderView::SelectAndPositionItems, SelectAndPositionItems, SelectAndPositionItems method [Windows Shell], SelectAndPositionItems method [Windows Shell],IFolderView interface, _shell_IFolderView_SelectAndPositionItems, shell.IFolderView_SelectAndPositionItems, shobjidl_core/IFolderView::SelectAndPositionItems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderView.SelectAndPositionItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView::SelectAndPositionItems


## -description


Allows the selection and positioning of items visible in the folder's view.


## -parameters




### -param cidl [in]

Type: <b>UINT</b>

The number of items to select.


### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of size <i>cidl</i> that contains the PIDLs of the items.


### -param apt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to an array of <i>cidl</i> structures containing the locations each corresponding element in <i>apidl</i> should be positioned.


### -param dwFlags [in]

Type: <b>DWORD</b>

One of the <a href="https://msdn.microsoft.com/3b0a7ec3-f365-48ec-86b0-ffd4c345deaf">_SVSIF</a> constants that specifies the type of selection to apply.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a>



<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>



<a href="https://msdn.microsoft.com/6db262ea-861b-4bc5-955f-b81945313ea8">IFolderView::SelectItem</a>



<a href="https://msdn.microsoft.com/5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f">SelectItem</a>
 

 


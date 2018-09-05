---
UID: NF:shlobj_core.IShellFolderView.ArrangeGrid
title: IShellFolderView::ArrangeGrid
author: windows-sdk-content
description: Arranges moved icons so that they align to an invisible grid.
old-location: shell\IShellFolderView_ArrangeGrid.htm
old-project: shell
ms.assetid: 3cb77a02-82da-42d3-97a3-ff47a9ce1831
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ArrangeGrid, ArrangeGrid method [Windows Shell], ArrangeGrid method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],ArrangeGrid method, IShellFolderView.ArrangeGrid, IShellFolderView::ArrangeGrid, _shell_IShellFolderView_ArrangeGrid, shell.IShellFolderView_ArrangeGrid, shlobj_core/IShellFolderView::ArrangeGrid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.ArrangeGrid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderView::ArrangeGrid


## -description


<p class="CCE_Message">[<b>ArrangeGrid</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Arranges moved icons so that they align to an invisible grid.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method has the same effect as selecting <b>View | Arrange Icons By | Align to Grid</b> in Windows Explorer on Windows XP, and also the same as right-clicking the desktop and selecting <b>Arrange Icons By | Align to Grid</b> on Windows XP or Windows Vista.




## -see-also




<a href="https://msdn.microsoft.com/e3b0b35f-6707-4e37-8470-31b1d4421d07">IShellFolderView</a>



<a href="https://msdn.microsoft.com/37260573-bac0-462c-a0df-654e2b22ed47">IShellFolderView::AutoArrange</a>
 

 


---
UID: NF:shlobj_core.IShellFolderView.AutoArrange
title: IShellFolderView::AutoArrange
author: windows-sdk-content
description: AutoArrange may be altered or unavailable.
old-location: shell\IShellFolderView_AutoArrange.htm
tech.root: shell
ms.assetid: 37260573-bac0-462c-a0df-654e2b22ed47
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AutoArrange, AutoArrange method [Windows Shell], AutoArrange method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],AutoArrange method, IShellFolderView.AutoArrange, IShellFolderView::AutoArrange, _shell_IShellFolderView_AutoArrange, shell.IShellFolderView_AutoArrange, shlobj_core/IShellFolderView::AutoArrange
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
 - shlobj_core.h
api_name:
 - IShellFolderView.AutoArrange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::AutoArrange


## -description


<p class="CCE_Message">[<b>AutoArrange</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Arranges moved icons so that they tend toward the left side of the viewing area and displace other icons with which they come into contact.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if the view is not in Auto Arrange mode, or an error value otherwise.




## -remarks



This method has the same effect as selecting <b>View | Arrange Icons By | Auto Arrange</b> in Windows Explorer on Windows XP, and also the same as right-clicking the desktop and selecting <b>Arrange Icons By | Auto Arrange</b> on Windows XP or Windows Vista.




## -see-also




<a href="https://msdn.microsoft.com/e3b0b35f-6707-4e37-8470-31b1d4421d07">IShellFolderView</a>



<a href="https://msdn.microsoft.com/3cb77a02-82da-42d3-97a3-ff47a9ce1831">IShellFolderView::ArrangeGrid</a>
 

 


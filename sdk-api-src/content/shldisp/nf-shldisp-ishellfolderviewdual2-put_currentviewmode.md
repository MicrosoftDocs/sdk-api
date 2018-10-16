---
UID: NF:shldisp.IShellFolderViewDual2.put_CurrentViewMode
title: IShellFolderViewDual2::put_CurrentViewMode
author: windows-sdk-content
description: Sets the current view mode of the current folder.
old-location: shell\IShellFolderViewDual2_put_CurrentViewMode.htm
tech.root: shell
ms.assetid: 80f0e24e-8104-472e-b1d9-58d42f3925fe
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IShellFolderViewDual2 interface [Windows Shell],put_CurrentViewMode method, IShellFolderViewDual2.put_CurrentViewMode, IShellFolderViewDual2::put_CurrentViewMode, _shell_IShellFolderViewDual2_put_CurrentViewMode, put_CurrentViewMode, put_CurrentViewMode method [Windows Shell], put_CurrentViewMode method [Windows Shell],IShellFolderViewDual2 interface, shell.IShellFolderViewDual2_put_CurrentViewMode, shldisp/IShellFolderViewDual2::put_CurrentViewMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - Shldisp.h
api_name:
 - IShellFolderViewDual2.put_CurrentViewMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderViewDual2::put_CurrentViewMode


## -description


Sets the current view mode of the current folder.


## -parameters




### -param ViewMode [in]

Type: <b>uint</b>

Sets the current view mode. For a list of possible values see <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f53b779e-a015-4b17-b04d-e0739cba8168">IShellFolderViewDual2</a>



<a href="https://msdn.microsoft.com/aa4bcb25-98f9-49c3-be25-abc6a5ecdcca">IShellFolderViewDual2::get_CurrentViewMode</a>
 

 


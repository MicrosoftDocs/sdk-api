---
UID: NF:shldisp.IShellFolderViewDual3.FilterView
title: IShellFolderViewDual3::FilterView
author: windows-sdk-content
description: Sets the filter on the contents of the current view.
old-location: shell\IShellFolderViewDual3_FilterView.htm
tech.root: shell
ms.assetid: 60808015-317e-469f-aa28-a2c2bfdb16a8
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: FilterView, FilterView method [Windows Shell], FilterView method [Windows Shell],IShellFolderViewDual3 interface, IShellFolderViewDual3 interface [Windows Shell],FilterView method, IShellFolderViewDual3.FilterView, IShellFolderViewDual3::FilterView, _shell_IShellFolderViewDual3_FilterView, shell.IShellFolderViewDual3_FilterView, shldisp/IShellFolderViewDual3::FilterView
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IShellFolderViewDual3.FilterView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderViewDual3::FilterView


## -description


Sets the filter on the contents of the current view.


## -parameters




### -param bstrFilterText [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a></b>

The BSTR that names the filter view for the current folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




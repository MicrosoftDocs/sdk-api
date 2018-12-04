---
UID: NF:shlobj_core.IShellFolderView.GetObjectCount
title: IShellFolderView::GetObjectCount
author: windows-sdk-content
description: Gets the number of items in the folder view.
old-location: shell\IShellFolderView_GetObjectCount.htm
tech.root: shell
ms.assetid: a68dca56-ae89-4280-b1de-8c85362bf9c6
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetObjectCount, GetObjectCount method [Windows Shell], GetObjectCount method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetObjectCount method, IShellFolderView.GetObjectCount, IShellFolderView::GetObjectCount, _shell_IShellFolderView_GetObjectCount, shell.IShellFolderView_GetObjectCount, shlobj_core/IShellFolderView::GetObjectCount
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
 - IShellFolderView.GetObjectCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::GetObjectCount


## -description


<p class="CCE_Message">[<b>GetObjectCount</b> is no longer available for use as of Windows Vista. Instead, use <a href="https://msdn.microsoft.com/dadf91c5-7d27-4b1b-875b-6f0615440f47">ItemCount</a>.]

Gets the number of items in the folder view.


## -parameters




### -param puCount [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of items displayed in the folder view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




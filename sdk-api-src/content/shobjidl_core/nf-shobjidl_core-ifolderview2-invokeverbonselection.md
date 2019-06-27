---
UID: NF:shobjidl_core.IFolderView2.InvokeVerbOnSelection
title: IFolderView2::InvokeVerbOnSelection (shobjidl_core.h)
author: windows-sdk-content
description: Invokes the given verb on the current selection.
old-location: shell\IFolderView2_InvokeVerbOnSelection.htm
tech.root: shell
ms.assetid: 085a08f9-c6a2-417c-973a-d0df84d8c821
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],InvokeVerbOnSelection method, IFolderView2.InvokeVerbOnSelection, IFolderView2::InvokeVerbOnSelection, InvokeVerbOnSelection, InvokeVerbOnSelection method [Windows Shell], InvokeVerbOnSelection method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_InvokeVerbOnSelection, shell.IFolderView2_InvokeVerbOnSelection, shobjidl_core/IFolderView2::InvokeVerbOnSelection
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IFolderView2.InvokeVerbOnSelection"
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
 - IFolderView2.InvokeVerbOnSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderView2::InvokeVerbOnSelection


## -description


Invokes the given verb on the current selection.


## -parameters




### -param pszVerb [in]

Type: <b>LPCSTR</b>

A pointer to a Unicode string containing a verb.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pszVerb</i> is <b>NULL</b>, then the default verb is invoked on the selection.




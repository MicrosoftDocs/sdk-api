---
UID: NF:shobjidl.IFolderViewHost.Initialize
title: IFolderViewHost::Initialize method
author: windows-driver-content
description: Initializes the object that hosts an IFolderView object.
old-location: shell\IFolderViewHost_Initialize.htm
old-project: shell
ms.assetid: 77740dfc-6423-451d-859b-7c894122309d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IFolderViewHost, IFolderViewHost interface [Windows Shell], Initialize method, IFolderViewHost::Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell], IFolderViewHost interface, Initialize,IFolderViewHost.Initialize, _shell_IFolderViewHost_Initialize, shell.IFolderViewHost_Initialize, shobjidl/IFolderViewHost::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IFolderViewHost.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IFolderViewHost::Initialize method


## -description


Initializes the object that hosts an <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a> object.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

The handle of the window that contains the <a href="https://msdn.microsoft.com/1e3d4a9a-6336-4667-92dd-9dc9678606e9">IFolderViewHost</a> object.


### -param pdo [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

The address of a pointer to a data object.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>


          The address of a pointer to a <b>RECT</b> structure that specifies the dimensions of the folder view.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




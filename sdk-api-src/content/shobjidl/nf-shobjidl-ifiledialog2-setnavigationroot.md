---
UID: NF:shobjidl.IFileDialog2.SetNavigationRoot
title: IFileDialog2::SetNavigationRoot
author: windows-driver-content
description: Specifies a top-level location from which to begin browsing a namespace, for instance in the Save dialog's Browse folder option. Users cannot navigate above this location.
old-location: shell\IFileDialog2_SetNavigationRoot.htm
old-project: shell
ms.assetid: 2ca6b5e7-5867-40f7-a949-e76815407005
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IFileDialog2 interface [Windows Shell],SetNavigationRoot method, IFileDialog2.SetNavigationRoot, IFileDialog2::SetNavigationRoot, SetNavigationRoot, SetNavigationRoot method [Windows Shell], SetNavigationRoot method [Windows Shell],IFileDialog2 interface, _shell_IFileDialog2_SetNavigationRoot, shell.IFileDialog2_SetNavigationRoot, shobjidl/IFileDialog2::SetNavigationRoot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comdlg32.dll
api_name:
-	IFileDialog2.SetNavigationRoot
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll (version 6.1 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IFileDialog2::SetNavigationRoot


## -description


Specifies a top-level location from which to begin browsing a namespace, for instance in the <b>Save</b> dialog's <b>Browse folder</b> option. Users cannot navigate above this location.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a></b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the navigation root.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SetNavigationRoot</b> can be used by applications that want to restrict navigation to a certain area of the Shell namespace. Items in the navigation pane are replaced with the supplied item, to guide the user from navigating outside of this part of the namespace.

This method cannot be called while the dialog is being displayed.




## -see-also




<a href="https://msdn.microsoft.com/be67a020-285d-4c1e-a8b5-8e1e90fae594">IFileDialog2</a>
 

 


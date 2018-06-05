---
UID: NF:shobjidl_core.IFileDialog.GetOptions
title: IFileDialog::GetOptions
author: windows-sdk-content
description: Gets the current flags that are set to control dialog behavior.
old-location: shell\IFileDialog_GetOptions.htm
old-project: shell
ms.assetid: 8a01b64d-b58e-4470-a5ed-8cf821b26c6b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetOptions method, IFileDialog.GetOptions, IFileDialog::GetOptions, shell.IFileDialog_GetOptions, shell_IFileDialog_GetOptions, shobjidl_core/IFileDialog::GetOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileDialog.GetOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::GetOptions


## -description


Gets the current flags that are set to control dialog behavior.


## -parameters




### -param pfos






#### - fos [out]

Type: <b>FILEOPENDIALOGOPTIONS*</b>

When this method returns successfully, points to a value made up of one or more of the <a href="https://msdn.microsoft.com/CDDB4B39-AFB9-4C0D-9D5A-0F2EA9EABE64">FILEOPENDIALOGOPTIONS</a> values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




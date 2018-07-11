---
UID: NF:shobjidl_core.IFileDialogCustomize.AddRadioButtonList
title: IFileDialogCustomize::AddRadioButtonList
author: windows-sdk-content
description: Adds an option button (also known as radio button) group to the dialog.
old-location: shell\IFileDialogCustomize_AddRadioButtonList.htm
old-project: shell
ms.assetid: 9f60b69d-4625-48b7-b265-ab2e9d842fc2
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: AddRadioButtonList, AddRadioButtonList method [Windows Shell], AddRadioButtonList method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddRadioButtonList method, IFileDialogCustomize.AddRadioButtonList, IFileDialogCustomize::AddRadioButtonList, shell.IFileDialogCustomize_AddRadioButtonList, shell_IFileDialogCustomize_AddRadioButtonList, shobjidl_core/IFileDialogCustomize::AddRadioButtonList
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.AddRadioButtonList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::AddRadioButtonList


## -description


Adds an option button (also known as radio button) group to the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>


                  The ID of the option button group to add.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default state for this control is enabled and visible.




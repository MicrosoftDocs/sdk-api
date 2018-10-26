---
UID: NF:shobjidl_core.IFileSaveDialog.SetCollectedProperties
title: IFileSaveDialog::SetCollectedProperties
author: windows-sdk-content
description: Specifies which properties will be collected in the save dialog.
old-location: shell\IFileSaveDialog_SetCollectedProperties.htm
tech.root: shell
ms.assetid: cff40aba-6a87-4c20-957d-6729e0d995ae
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetCollectedProperties method, IFileSaveDialog.SetCollectedProperties, IFileSaveDialog::SetCollectedProperties, SetCollectedProperties, SetCollectedProperties method [Windows Shell], SetCollectedProperties method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetCollectedProperties, shell_IFileSaveDialog_SetCollectedProperties, shobjidl_core/IFileSaveDialog::SetCollectedProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
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
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.SetCollectedProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSaveDialog::SetCollectedProperties


## -description


Specifies which properties will be collected in the save dialog.


## -parameters




### -param pList [in]

Type: <b><a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a>*</b>

Pointer to the interface that represents the list of properties to collect. This parameter can be <b>NULL</b>.


### -param fAppendDefault [in]

Type: <b>BOOL</b>

<b>TRUE</b> to show default properties for the currently selected filetype in addition to the properties specified by <i>pList</i>. <b>FALSE</b> to show only properties specified by <i>pList</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The calling application can use the <a href="https://msdn.microsoft.com/348253ed-46ac-4643-bbf8-2d286ae97f07">PSGetPropertyDescriptionListFromString</a> function to construct an <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a> from a string such as "prop:Comments;Subject;".

For more information about property schemas, see 
            <a href="https://msdn.microsoft.com/4e301210-df3a-41db-a58e-015ee8d41714">Property Schemas</a>.

<b>IFileSaveDialog::SetCollectedProperties</b> can be called at any time before the dialog is displayed or while it is visible. If different properties are to be collected depending on the chosen filetype, then <b>IFileSaveDialog::SetCollectedProperties</b> can be called in response to <a href="https://msdn.microsoft.com/d57e7b57-520d-40d6-8bac-ebf245ad7484">OnTypeChange</a>.

<div class="alert"><b>Note</b>  By default, no properties are collected in the save dialog.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/74021f92-54ff-4c02-a8cf-49bcd7b9171e">IFileSaveDialog</a>



<a href="https://msdn.microsoft.com/418f2524-5e6d-4e79-894b-b5f706171836">IFileSaveDialog::SetProperties</a>
 

 


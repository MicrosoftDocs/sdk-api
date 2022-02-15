---
UID: NF:shobjidl_core.IFileSaveDialog.SetCollectedProperties
title: IFileSaveDialog::SetCollectedProperties (shobjidl_core.h)
description: Specifies which properties will be collected in the save dialog.
helpviewer_keywords: ["IFileSaveDialog interface [Windows Shell]","SetCollectedProperties method","IFileSaveDialog.SetCollectedProperties","IFileSaveDialog::SetCollectedProperties","SetCollectedProperties","SetCollectedProperties method [Windows Shell]","SetCollectedProperties method [Windows Shell]","IFileSaveDialog interface","shell.IFileSaveDialog_SetCollectedProperties","shell_IFileSaveDialog_SetCollectedProperties","shobjidl_core/IFileSaveDialog::SetCollectedProperties"]
old-location: shell\IFileSaveDialog_SetCollectedProperties.htm
tech.root: shell
ms.assetid: cff40aba-6a87-4c20-957d-6729e0d995ae
ms.date: 12/05/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetCollectedProperties method, IFileSaveDialog.SetCollectedProperties, IFileSaveDialog::SetCollectedProperties, SetCollectedProperties, SetCollectedProperties method [Windows Shell], SetCollectedProperties method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetCollectedProperties, shell_IFileSaveDialog_SetCollectedProperties, shobjidl_core/IFileSaveDialog::SetCollectedProperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSaveDialog::SetCollectedProperties
 - shobjidl_core/IFileSaveDialog::SetCollectedProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.SetCollectedProperties
---

# IFileSaveDialog::SetCollectedProperties


## -description

Specifies which properties will be collected in the save dialog.

## -parameters

### -param pList [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>*</b>

Pointer to the interface that represents the list of properties to collect. This parameter can be <b>NULL</b>.

### -param fAppendDefault [in]

Type: <b>BOOL</b>

<b>TRUE</b> to show default properties for the currently selected filetype in addition to the properties specified by <i>pList</i>. <b>FALSE</b> to show only properties specified by <i>pList</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The calling application can use the <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a> function to construct an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> from a string such as "prop:Comments;Subject;".

For more information about property schemas, see 
            <a href="/windows/desktop/properties/building-property-handlers-property-schemas">Property Schemas</a>.

<b>IFileSaveDialog::SetCollectedProperties</b> can be called at any time before the dialog is displayed or while it is visible. If different properties are to be collected depending on the chosen filetype, then <b>IFileSaveDialog::SetCollectedProperties</b> can be called in response to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-ontypechange">OnTypeChange</a>.

<div class="alert"><b>Note</b>  By default, no properties are collected in the save dialog.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setproperties">IFileSaveDialog::SetProperties</a>
---
UID: NF:shobjidl_core.IFileOperation.SetProperties
title: IFileOperation::SetProperties (shobjidl_core.h)
description: Declares a set of properties and values to be set on an item or items.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","SetProperties method","IFileOperation.SetProperties","IFileOperation::SetProperties","SetProperties","SetProperties method [Windows Shell]","SetProperties method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_SetProperties","shell.IFileOperation_SetProperties","shobjidl_core/IFileOperation::SetProperties"]
old-location: shell\IFileOperation_SetProperties.htm
tech.root: shell
ms.assetid: b54efc12-42e9-4a90-a4d9-0e75bcdba0d6
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],SetProperties method, IFileOperation.SetProperties, IFileOperation::SetProperties, SetProperties, SetProperties method [Windows Shell], SetProperties method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetProperties, shell.IFileOperation_SetProperties, shobjidl_core/IFileOperation::SetProperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperation::SetProperties
 - shobjidl_core/IFileOperation::SetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.SetProperties
---

# IFileOperation::SetProperties


## -description

Declares a set of properties and values to be set on an item or items.

## -parameters

### -param pproparray [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a>*</b>

Pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychangearray">IPropertyChangeArray</a>, which accesses a collection of <a href="/windows/desktop/api/propsys/nn-propsys-ipropertychange">IPropertyChange</a> objects that specify the properties to be set and their new values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not set the new property values, it merely declares them. To set property values on an item or a group of items, you must make at least the sequence of calls detailed here:

                

<ol>
<li>Call <b>IFileOperation::SetProperties</b> to declare the specific properties to be set and their new values.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitem">IFileOperation::ApplyPropertiesToItem</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitems">IFileOperation::ApplyPropertiesToItems</a> to declare the item or items whose properties are to be set.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to apply the properties to the item or items.</li>
</ol>
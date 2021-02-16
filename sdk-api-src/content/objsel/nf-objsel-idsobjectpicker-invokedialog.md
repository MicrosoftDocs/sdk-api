---
UID: NF:objsel.IDsObjectPicker.InvokeDialog
title: IDsObjectPicker::InvokeDialog (objsel.h)
description: Displays a modal object picker dialog box and returns the user selections.
helpviewer_keywords: ["IDsObjectPicker interface [Active Directory]","InvokeDialog method","IDsObjectPicker.InvokeDialog","IDsObjectPicker::InvokeDialog","InvokeDialog","InvokeDialog method [Active Directory]","InvokeDialog method [Active Directory]","IDsObjectPicker interface","_glines_idsobjectpicker_invokedialog","ad.idsobjectpicker__invokedialog","ad.idsobjectpicker_invokedialog","objsel/IDsObjectPicker::InvokeDialog"]
old-location: ad\idsobjectpicker_invokedialog.htm
tech.root: ad
ms.assetid: 76192a35-10e1-46e3-8724-7637d47d8eca
ms.date: 12/05/2018
ms.keywords: IDsObjectPicker interface [Active Directory],InvokeDialog method, IDsObjectPicker.InvokeDialog, IDsObjectPicker::InvokeDialog, InvokeDialog, InvokeDialog method [Active Directory], InvokeDialog method [Active Directory],IDsObjectPicker interface, _glines_idsobjectpicker_invokedialog, ad.idsobjectpicker__invokedialog, ad.idsobjectpicker_invokedialog, objsel/IDsObjectPicker::InvokeDialog
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Objsel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsObjectPicker::InvokeDialog
 - objsel/IDsObjectPicker::InvokeDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPicker.InvokeDialog
---

# IDsObjectPicker::InvokeDialog


## -description

The <b>IDsObjectPicker::InvokeDialog</b> method displays a modal object picker dialog box and returns the user selections.

## -parameters

### -param hwndParent

Handle to the owner window of the dialog box. This parameter cannot be <b>NULL</b> or the result of the <a href="/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a> function.

### -param ppdoSelections

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface pointer that receives a data object that contains data about the user selections. This data is supplied in the <a href="/windows/desktop/AD/cfstr-dsop-ds-selection-list">CFSTR_DSOP_DS_SELECTION_LIST</a> data format. This parameter receives <b>NULL</b> if the user cancels the dialog box.

## -returns

Returns a standard error code or one of the following values.

## -remarks

Before <b>IDsObjectPicker::InvokeDialog</b> is called, the <a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpicker">IDsObjectPicker</a> object must be initialized by calling <a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a>. After the <b>IDsObjectPicker</b> object is initialized, <b>InvokeDialog</b> can be called multiple times without reinitializing the interface.

## -see-also

<a href="/windows/desktop/AD/cfstr-dsop-ds-selection-list">CFSTR_DSOP_DS_SELECTION_LIST</a>



<a href="/windows/desktop/api/objsel/ns-objsel-ds_selection">DS_SELECTION</a>



<a href="/windows/desktop/api/objsel/ns-objsel-ds_selection_list">DS_SELECTION_LIST</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/objsel/nn-objsel-idsobjectpicker">IDsObjectPicker</a>
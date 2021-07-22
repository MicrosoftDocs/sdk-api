---
UID: NF:shobjidl_core.IShellItemArray.BindToHandler
title: IShellItemArray::BindToHandler (shobjidl_core.h)
description: Binds to an object by means of the specified handler.
helpviewer_keywords: ["BHID_AssociationArray","BHID_DataObject","BHID_SFUIObject","BindToHandler","BindToHandler method [Windows Shell]","BindToHandler method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","BindToHandler method","IShellItemArray.BindToHandler","IShellItemArray::BindToHandler","_shell_IShellItemArray_BindToHandler","shell.IShellItemArray_BindToHandler","shobjidl_core/IShellItemArray::BindToHandler"]
old-location: shell\IShellItemArray_BindToHandler.htm
tech.root: shell
ms.assetid: 7632d876-c00b-4dfc-862b-9a68f01bd8da
ms.date: 12/05/2018
ms.keywords: BHID_AssociationArray, BHID_DataObject, BHID_SFUIObject, BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],BindToHandler method, IShellItemArray.BindToHandler, IShellItemArray::BindToHandler, _shell_IShellItemArray_BindToHandler, shell.IShellItemArray_BindToHandler, shobjidl_core/IShellItemArray::BindToHandler
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
 - IShellItemArray::BindToHandler
 - shobjidl_core/IShellItemArray::BindToHandler
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
 - IShellItemArray.BindToHandler
---

# IShellItemArray::BindToHandler


## -description

Binds to an object by means of the specified handler.

## -parameters

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object.

### -param bhid [in]

Type: <b>REFGUID</b>

One of the following values, defined in Shlguid.h, that determine the handler.



#### BHID_SFUIObject

Restricts usage to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">GetUIObjectOf</a>. Use this handler type only for a flat item array, where all items are in the same folder.



#### BHID_DataObject

<b>Introduced in Windows Vista</b>: Gets an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object for use with an item or an array of items. Use this handler type only for flat data objects or item arrays created by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject">SHCreateShellItemArrayFromDataObject</a>.



#### BHID_AssociationArray

<b>Introduced in Windows Vista</b>: Gets an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> object for use with an item or an array of items. This only retrieves the association array object for the first item in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>

### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.

### -param ppvOut [out]

Type: <b>void**</b>

When this methods returns, contains the object specified in <i>riid</i> that is returned by the handler specified by <i>rbhid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
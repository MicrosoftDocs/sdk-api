---
UID: NF:shobjidl_core.IShellItem.BindToHandler
title: IShellItem::BindToHandler (shobjidl_core.h)
description: Binds to a handler for an item as specified by the handler ID value (BHID).
helpviewer_keywords: ["BHID_AssociationArray","BHID_DataObject","BHID_EnumAssocHandlers","BHID_EnumItems","BHID_FilePlaceholder","BHID_Filter","BHID_LinkTargetItem","BHID_PropertyStore","BHID_RandomAccessStream","BHID_SFObject","BHID_SFUIObject","BHID_SFViewObject","BHID_Storage","BHID_StorageEnum","BHID_Stream","BHID_ThumbnailHandler","BHID_Transfer","BindToHandler","BindToHandler method [Windows Shell]","BindToHandler method [Windows Shell]","IShellItem interface","IShellItem interface [Windows Shell]","BindToHandler method","IShellItem.BindToHandler","IShellItem::BindToHandler","_win32_IShellItem_BindToHandler","shell.IShellItem_BindToHandler","shobjidl_core/IShellItem::BindToHandler"]
old-location: shell\IShellItem_BindToHandler.htm
tech.root: shell
ms.assetid: fadd70cd-5018-4b71-af7b-d9c780ebddc5
ms.date: 12/05/2018
ms.keywords: BHID_AssociationArray, BHID_DataObject, BHID_EnumAssocHandlers, BHID_EnumItems, BHID_FilePlaceholder, BHID_Filter, BHID_LinkTargetItem, BHID_PropertyStore, BHID_RandomAccessStream, BHID_SFObject, BHID_SFUIObject, BHID_SFViewObject, BHID_Storage, BHID_StorageEnum, BHID_Stream, BHID_ThumbnailHandler, BHID_Transfer, BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],BindToHandler method, IShellItem.BindToHandler, IShellItem::BindToHandler, _win32_IShellItem_BindToHandler, shell.IShellItem_BindToHandler, shobjidl_core/IShellItem::BindToHandler
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem::BindToHandler
 - shobjidl_core/IShellItem::BindToHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellItem.BindToHandler
---

# IShellItem::BindToHandler


## -description

Binds to a handler for an item as specified by the handler ID value (BHID).

## -parameters

### -param pbc

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object. Used to pass optional parameters to the handler. The contents of the bind context are handler-specific. For example, when binding to <b>BHID_Stream</b>, the <a href="/windows/desktop/Stg/stgm-constants">STGM</a> flags in the bind context indicate the mode of access desired (read or read/write).

### -param bhid

Type: <b>REFGUID</b>

Reference to a GUID that specifies which handler will be created. One of the following values defined in Shlguid.h:



#### BHID_SFObject

Restricts usage to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">BindToObject</a>.



#### BHID_SFUIObject

Restricts usage to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">GetUIObjectOf</a>.



#### BHID_SFViewObject

Restricts usage to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">CreateViewObject</a>.



#### BHID_Storage

Attempts to retrieve the storage RIID, but defaults to Shell implementation on failure.



#### BHID_Stream

Restricts usage to <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.



#### BHID_LinkTargetItem

CLSID_ShellItem is initialized with the target of this item (can only be SFGAO_LINK). See <a href="/windows/win32/shell/sfgao">SFGAO</a> for a description of SFGAO_LINK.



#### BHID_StorageEnum

If the item is a folder, gets an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object with which to enumerate the storage contents.



#### BHID_Transfer

<b>Introduced in Windows Vista</b>: If the item is a folder, gets an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a> object.



#### BHID_PropertyStore

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorefactory">IPropertyStoreFactory</a>.



#### BHID_ThumbnailHandler

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> or <a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailprovider">IThumbnailProvider</a>.



#### BHID_EnumItems

<b>Introduced in Windows Vista</b>: If the item is a folder, gets an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object that enumerates all items in the folder. This includes folders, nonfolders, and hidden items.



#### BHID_DataObject

<b>Introduced in Windows Vista</b>: Gets an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object for use with an item or an array of items.



#### BHID_AssociationArray

<b>Introduced in Windows Vista</b>: Gets an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> object for use with an item or an array of items.



#### BHID_Filter

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>.



#### BHID_EnumAssocHandlers

<b>Introduced in Windows 7</b>: Gets an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers">IEnumAssocHandlers</a> object used to enumerate the recommended association handlers for the given item.



#### BHID_RandomAccessStream

<b>Introduced in Windows 8</b>: Gets an <a href="/previous-versions/hh438400(v=vs.85)">IRandomAccessStream</a> object for the item.



#### BHID_FilePlaceholder

<b>Introduced in Windows 8.1</b>: Gets an object used to provide placeholder file functionality.

### -param riid

Type: <b>REFIID</b>

IID of the object type to retrieve.

### -param ppv

Type: <b>void**</b>

When this method returns, contains a pointer of type <i>riid</i> that is returned by the handler specified by <i>rbhid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>

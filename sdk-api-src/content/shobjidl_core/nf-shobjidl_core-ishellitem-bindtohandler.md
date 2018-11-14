---
UID: NF:shobjidl_core.IShellItem.BindToHandler
title: IShellItem::BindToHandler
author: windows-sdk-content
description: Binds to a handler for an item as specified by the handler ID value (BHID).
old-location: shell\IShellItem_BindToHandler.htm
tech.root: shell
ms.assetid: fadd70cd-5018-4b71-af7b-d9c780ebddc5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: BHID_AssociationArray, BHID_DataObject, BHID_EnumAssocHandlers, BHID_EnumItems, BHID_FilePlaceholder, BHID_Filter, BHID_LinkTargetItem, BHID_PropertyStore, BHID_RandomAccessStream, BHID_SFObject, BHID_SFUIObject, BHID_SFViewObject, BHID_Storage, BHID_StorageEnum, BHID_Stream, BHID_ThumbnailHandler, BHID_Transfer, BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],BindToHandler method, IShellItem.BindToHandler, IShellItem::BindToHandler, _win32_IShellItem_BindToHandler, shell.IShellItem_BindToHandler, shobjidl_core/IShellItem::BindToHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellItem.BindToHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IShellItem.BindToHandler
: 
---

# IShellItem::BindToHandler


## -description


Binds to a handler for an item as specified by the handler ID value (BHID).


## -parameters




### -param pbc

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object. Used to pass optional parameters to the handler. The contents of the bind context are handler-specific. For example, when binding to <b>BHID_Stream</b>, the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> flags in the bind context indicate the mode of access desired (read or read/write).


### -param bhid

TBD


### -param riid

Type: <b>REFIID</b>

IID of the object type to retrieve.


### -param ppv

TBD




#### - ppvOut

Type: <b>void**</b>

When this method returns, contains a pointer of type <i>riid</i> that is returned by the handler specified by <i>rbhid</i>.


#### - rbhid

Type: <b>REFGUID</b>

Reference to a GUID that specifies which handler will be created. One of the following values defined in Shlguid.h:



#### BHID_SFObject

Restricts usage to <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">BindToObject</a>.



#### BHID_SFUIObject

Restricts usage to <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">GetUIObjectOf</a>.



#### BHID_SFViewObject

Restricts usage to <a href="https://msdn.microsoft.com/8a1b73ad-6719-403a-a8aa-27bef537b7a9">CreateViewObject</a>.



#### BHID_Storage

Attempts to retrieve the storage RIID, but defaults to Shell implementation on failure.



#### BHID_Stream

Restricts usage to <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.



#### BHID_LinkTargetItem

CLSID_ShellItem is initialized with the target of this item (can only be SFGAO_LINK). See <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">GetAttributesOf</a> for a description of SFGAO_LINK.



#### BHID_StorageEnum

If the item is a folder, gets an <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object with which to enumerate the storage contents.



#### BHID_Transfer

<b>Introduced in Windows Vista</b>: If the item is a folder, gets an <a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a> or <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a> object.



#### BHID_PropertyStore

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> or <a href="https://msdn.microsoft.com/78ea822d-da8e-4883-b0eb-4277e7eb87a2">IPropertyStoreFactory</a>.



#### BHID_ThumbnailHandler

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a> or <a href="https://msdn.microsoft.com/55c4739a-4835-4f53-a435-804ddf06ffcf">IThumbnailProvider</a>.



#### BHID_EnumItems

<b>Introduced in Windows Vista</b>: If the item is a folder, gets an <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> object that enumerates all items in the folder. This includes folders, nonfolders, and hidden items.



#### BHID_DataObject

<b>Introduced in Windows Vista</b>: Gets an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> object for use with an item or an array of items.



#### BHID_AssociationArray

<b>Introduced in Windows Vista</b>: Gets an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> object for use with an item or an array of items.



#### BHID_Filter

<b>Introduced in Windows Vista</b>: Restricts usage to <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>.



#### BHID_EnumAssocHandlers

<b>Introduced in Windows 7</b>: Gets an <a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a> object used to enumerate the recommended association handlers for the given item.



#### BHID_RandomAccessStream

<b>Introduced in Windows 8</b>: Gets an <a href="https://msdn.microsoft.com/a9a4bd11-8c69-4826-9ea0-6f42421c8367">IRandomAccessStream</a> object for the item.



#### BHID_FilePlaceholder

<b>Introduced in Windows 8.1</b>: Gets an object used to provide placeholder file functionality.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 


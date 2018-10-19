---
UID: NF:shobjidl_core.IShellItemArray.BindToHandler
title: IShellItemArray::BindToHandler
author: windows-sdk-content
description: Binds to an object by means of the specified handler.
old-location: shell\IShellItemArray_BindToHandler.htm
tech.root: shell
ms.assetid: 7632d876-c00b-4dfc-862b-9a68f01bd8da
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: BHID_AssociationArray, BHID_DataObject, BHID_SFUIObject, BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],BindToHandler method, IShellItemArray.BindToHandler, IShellItemArray::BindToHandler, _shell_IShellItemArray_BindToHandler, shell.IShellItemArray_BindToHandler, shobjidl_core/IShellItemArray::BindToHandler
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray.BindToHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemArray::BindToHandler


## -description


Binds to an object by means of the specified handler.


## -parameters




### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object.


### -param bhid

TBD


### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.


### -param ppvOut [out]

Type: <b>void**</b>

When this methods returns, contains the object specified in <i>riid</i> that is returned by the handler specified by <i>rbhid</i>.


#### - rbhid [in]

Type: <b>REFGUID</b>

One of the following values, defined in Shlguid.h, that determine the handler.



#### BHID_SFUIObject

Restricts usage to <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">GetUIObjectOf</a>. Use this handler type only for a flat item array, where all items are in the same folder.



#### BHID_DataObject

<b>Introduced in Windows Vista</b>: Gets an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> object for use with an item or an array of items. Use this handler type only for flat data objects or item arrays created by <a href="https://msdn.microsoft.com/91e65c9a-0600-42e3-97f5-2a5960e1ec89">SHCreateShellItemArrayFromDataObject</a>.



#### BHID_AssociationArray

<b>Introduced in Windows Vista</b>: Gets an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> object for use with an item or an array of items. This only retrieves the association array object for the first item in the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




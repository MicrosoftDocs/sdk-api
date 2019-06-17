---
UID: NF:shobjidl_core.IShellFolder.BindToObject
title: IShellFolder::BindToObject (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves a handler, typically the Shell folder object that implements IShellFolder for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.
old-location: shell\IShellFolder_BindToObject.htm
tech.root: shell
ms.assetid: 5e699494-1974-4b9b-8324-9394f7b96fe4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BindToObject, BindToObject method [Windows Shell], BindToObject method [Windows Shell],IShellFolder interface, BindToObject method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],BindToObject method, IShellFolder.BindToObject, IShellFolder2 interface [Windows Shell],BindToObject method, IShellFolder2::BindToObject, IShellFolder::BindToObject, _win32_IShellFolder_BindToObject, shell.IShellFolder_BindToObject, shobjidl_core/IShellFolder2::BindToObject, shobjidl_core/IShellFolder::BindToObject
ms.topic: method
f1_keywords: ["shobjidl_core/IShellFolder.BindToObject"]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder.BindToObject
 - IShellFolder2.BindToObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolder::BindToObject


## -description


Retrieves a handler, typically the Shell folder object that implements <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a> structure (PIDL) that identifies the subfolder. This value can refer to an item at any level below the parent folder in the namespace hierarchy. The structure contains one or more <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_shitemid">SHITEMID</a> structures, followed by a terminating <b>NULL</b>.


### -param pbc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object that can be used to pass parameters to the construction of the handler. If this parameter is not used, set it to <b>NULL</b>. Because support for this parameter is optional for folder object implementations, some folders may not support the use of bind contexts. 

                    

Information that can be provided in the bind context includes a <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagbind_opts">BIND_OPTS</a> structure that includes a <b>grfMode</b> member that indicates the access mode when binding to a stream handler. Other parameters can be set and discovered using <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam">IBindCtx::GetObjectParam</a>.


### -param riid [in]

Type: <b>REFIID</b>

The identifier of the interface to return. This may be <b>IID_IShellFolder</b>, <b>IID_IStream</b>, or any other interface that identifies a particular handler.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested interface. If an error occurs, a <b>NULL</b> pointer is returned at this address.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use <b>IShellFolder::BindToObject</b><b>(..., IID_IShellFolder, ...)</b> to obtain the Shell folder object for a subitem. Clients should pass the canonical interface IID that is used to identify a specific handler. For example, <b>IID_IShellFolder</b> identifies the folder handler and <b>IID_IStream</b> identifies the stream handler. Implementations can support binding to handlers using derived interfaces as well, such as <b>IID_IShellFolder2</b>. A Shell namespace extension can implement this function by creating the Shell folder object for the specified subitem and then calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> to communicate with the object through its interface pointer.

Implementations of <b>BindToObject</b> can optimize any call to it by quickly failing for IID values that it does not support. For example, if the Shell folder object of the subitem does not support <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer">IRemoteComputer</a>, the implementation should return <b>E_NOINTERFACE</b> immediately instead of needlessly creating the Shell folder object for the subitem and then finding that <b>IRemoteComputer</b> was not supported after all.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a>
 

 


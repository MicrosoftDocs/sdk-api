---
UID: NF:shobjidl_core.IShellFolder.BindToObject
title: IShellFolder::BindToObject
author: windows-sdk-content
description: Retrieves a handler, typically the Shell folder object that implements IShellFolder for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.
old-location: shell\IShellFolder_BindToObject.htm
tech.root: shell
ms.assetid: 5e699494-1974-4b9b-8324-9394f7b96fe4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: BindToObject, BindToObject method [Windows Shell], BindToObject method [Windows Shell],IShellFolder interface, BindToObject method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],BindToObject method, IShellFolder.BindToObject, IShellFolder2 interface [Windows Shell],BindToObject method, IShellFolder2::BindToObject, IShellFolder::BindToObject, _win32_IShellFolder_BindToObject, shell.IShellFolder_BindToObject, shobjidl_core/IShellFolder2::BindToObject, shobjidl_core/IShellFolder::BindToObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IShellFolder::BindToObject


## -description


Retrieves a handler, typically the Shell folder object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

The address of an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure (PIDL) that identifies the subfolder. This value can refer to an item at any level below the parent folder in the namespace hierarchy. The structure contains one or more <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structures, followed by a terminating <b>NULL</b>.


### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on a bind context object that can be used to pass parameters to the construction of the handler. If this parameter is not used, set it to <b>NULL</b>. Because support for this parameter is optional for folder object implementations, some folders may not support the use of bind contexts. 

                    

Information that can be provided in the bind context includes a <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure that includes a <b>grfMode</b> member that indicates the access mode when binding to a stream handler. Other parameters can be set and discovered using <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a> and <a href="https://msdn.microsoft.com/8f423495-7a34-4901-968e-1fe204680d8a">IBindCtx::GetObjectParam</a>.


### -param riid [in]

Type: <b>REFIID</b>

The identifier of the interface to return. This may be <b>IID_IShellFolder</b>, <b>IID_IStream</b>, or any other interface that identifies a particular handler.


### -param ppv

TBD




#### - ppvOut [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested interface. If an error occurs, a <b>NULL</b> pointer is returned at this address.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use <b>IShellFolder::BindToObject</b><b>(..., IID_IShellFolder, ...)</b> to obtain the Shell folder object for a subitem. Clients should pass the canonical interface IID that is used to identify a specific handler. For example, <b>IID_IShellFolder</b> identifies the folder handler and <b>IID_IStream</b> identifies the stream handler. Implementations can support binding to handlers using derived interfaces as well, such as <b>IID_IShellFolder2</b>. A Shell namespace extension can implement this function by creating the Shell folder object for the specified subitem and then calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to communicate with the object through its interface pointer.

Implementations of <b>BindToObject</b> can optimize any call to it by quickly failing for IID values that it does not support. For example, if the Shell folder object of the subitem does not support <a href="https://msdn.microsoft.com/a2137043-baee-496b-b3ad-45af5a6f123e">IRemoteComputer</a>, the implementation should return <b>E_NOINTERFACE</b> immediately instead of needlessly creating the Shell folder object for the subitem and then finding that <b>IRemoteComputer</b> was not supported after all.




## -see-also




<a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>



<a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a>



<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a>



<a href="https://msdn.microsoft.com/121cbd41-d512-4f33-b89c-d0dd9933df87">SHGetDesktopFolder</a>
 

 


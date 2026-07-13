---
UID: NF:shobjidl_core.IShellFolder.CreateViewObject
title: IShellFolder::CreateViewObject (shobjidl_core.h)
description: Requests an object that can be used to obtain information from or interact with a folder object.
helpviewer_keywords: ["CreateViewObject","CreateViewObject method [Windows Shell]","CreateViewObject method [Windows Shell]","IShellFolder interface","CreateViewObject method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","CreateViewObject method","IShellFolder.CreateViewObject","IShellFolder2 interface [Windows Shell]","CreateViewObject method","IShellFolder2::CreateViewObject","IShellFolder::CreateViewObject","_win32_IShellFolder_CreateViewObject","shell.IShellFolder_CreateViewObject","shobjidl_core/IShellFolder2::CreateViewObject","shobjidl_core/IShellFolder::CreateViewObject"]
old-location: shell\IShellFolder_CreateViewObject.htm
tech.root: shell
ms.assetid: 8a1b73ad-6719-403a-a8aa-27bef537b7a9
ms.date: 12/05/2018
ms.keywords: CreateViewObject, CreateViewObject method [Windows Shell], CreateViewObject method [Windows Shell],IShellFolder interface, CreateViewObject method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],CreateViewObject method, IShellFolder.CreateViewObject, IShellFolder2 interface [Windows Shell],CreateViewObject method, IShellFolder2::CreateViewObject, IShellFolder::CreateViewObject, _win32_IShellFolder_CreateViewObject, shell.IShellFolder_CreateViewObject, shobjidl_core/IShellFolder2::CreateViewObject, shobjidl_core/IShellFolder::CreateViewObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::CreateViewObject
 - shobjidl_core/IShellFolder::CreateViewObject
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
 - IShellFolder.CreateViewObject
 - IShellFolder2.CreateViewObject
---

# IShellFolder::CreateViewObject


## -description

Requests an object that can be used to obtain information from or interact with a folder object.

## -parameters

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the owner window. If you have implemented a custom folder view object, your folder view window should be created as a child of <i>hwndOwner</i>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellView.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>. See the Remarks section for more details.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To support this request, create an object that exposes the interface indicated by <i>riid</i> and return a pointer to that interface.

The primary purpose of this method is to provide Windows Explorer with the folder object's folder view object. Windows Explorer requests a folder view object by setting <i>riid</i> to IID_IShellView. The folder view object displays the contents of the folder in the Windows Explorer folder view. The folder view object must be independent of the Shell folder object, because Windows Explorer may call this method more than once to create multiple folder view objects. A new view object must be created each time this method is called. Your folder object can respond in one of two ways to this request. It can:

				

<ul>
<li>Create a custom folder view object and return a pointer to its <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.</li>
<li>Create a system folder view object and return a pointer to its <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.</li>
</ul>
This method is also used to request objects that expose one of several optional interfaces, including <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> or <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a>. In this context, <b>CreateViewObject</b> is similar in usage to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a>. However, you call <b>IShellFolder::GetUIObjectOf</b> to request an object for one of the items contained by a folder. Call <b>IShellFolder::CreateViewObject</b> to request an object for the folder itself. The most commonly requested interfaces are:
        
                

<ul>
<li>
<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo">IQueryInfo</a>
</li>
<li>
<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails">IShellDetails</a>
</li>
<li>
<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>
</li>
</ul>
We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>
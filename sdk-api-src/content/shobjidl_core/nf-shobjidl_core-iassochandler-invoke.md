---
UID: NF:shobjidl_core.IAssocHandler.Invoke
title: IAssocHandler::Invoke (shobjidl_core.h)
description: Directly invokes the associated handler.
helpviewer_keywords: ["IAssocHandler interface [Windows Shell]","Invoke method","IAssocHandler.Invoke","IAssocHandler::Invoke","Invoke","Invoke method [Windows Shell]","Invoke method [Windows Shell]","IAssocHandler interface","_shell_IAssocHandler_Invoke","shell.IAssocHandler_Invoke","shobjidl_core/IAssocHandler::Invoke"]
old-location: shell\IAssocHandler_Invoke.htm
tech.root: shell
ms.assetid: 2d22c987-3a25-4a36-8411-eaed921d066e
ms.date: 12/05/2018
ms.keywords: IAssocHandler interface [Windows Shell],Invoke method, IAssocHandler.Invoke, IAssocHandler::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],IAssocHandler interface, _shell_IAssocHandler_Invoke, shell.IAssocHandler_Invoke, shobjidl_core/IAssocHandler::Invoke
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
 - IAssocHandler::Invoke
 - shobjidl_core/IAssocHandler::Invoke
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
 - IAssocHandler.Invoke
---

# IAssocHandler::Invoke


## -description

Directly invokes the associated handler.

## -parameters

### -param pdo [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> that represents the selected item on which to invoke the handler. Note that you should not call <b>IAssocHandler::Invoke</b> with a selection of multiple items. If you have multiple items, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-createinvoker">IAssocHandler::CreateInvoker</a> instead. See Remarks for more details.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a> objects are typically used to populate an <b>Open With</b> menu. When one of those menu items is selected, this method is called to launch the chosen application.

<h3><a id="Invoke_and_CreateInvoker"></a><a id="invoke_and_createinvoker"></a><a id="INVOKE_AND_CREATEINVOKER"></a>Invoke and CreateInvoker</h3>
The <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> used by these methods can represent either a single file or a selection of multiple files. Not all applications support the multiple file option. The applications that do support that scenario might impose other restrictions, such as the number of files that can be opened simultaneously, or the acceptable combination of file types.
              

Therefore, an application often must determine whether the handler supports the selection before trying to invoke the handler. For example, an application might enable a menu item only if it has verified that the selection in question was supported by that handler.

It is generally safe to assume that an application will support invocation on a single item, and in those cases the application typically calls <b>IAssocHandler::Invoke</b> based on that assumption.

For multiple selection scenarios, however, the application should call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-createinvoker">IAssocHandler::CreateInvoker</a>. That method retrieves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a> object that allows the calling application to first check whether the selection is supported (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandlerinvoker-supportsselection">SupportsSelection</a>), then to invoke the handler (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandlerinvoker-invoke">Invoke</a>).

<b>IAssocHandler::Invoke</b> can be called on a selection of multiple files, but it is not recommended because of the large processing load involved and no guarantee that it will succeed.
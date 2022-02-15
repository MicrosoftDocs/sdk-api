---
UID: NF:shobjidl_core.IAssocHandler.CreateInvoker
title: IAssocHandler::CreateInvoker (shobjidl_core.h)
description: Retrieves an object that enables the invocation of the associated handler on the current selection. The invoker includes the ability to verify whether the current selection is supported.
helpviewer_keywords: ["CreateInvoker","CreateInvoker method [Windows Shell]","CreateInvoker method [Windows Shell]","IAssocHandler interface","IAssocHandler interface [Windows Shell]","CreateInvoker method","IAssocHandler.CreateInvoker","IAssocHandler::CreateInvoker","_shell_IAssocHandler_CreateInvoker","shell.IAssocHandler_CreateInvoker","shobjidl_core/IAssocHandler::CreateInvoker"]
old-location: shell\IAssocHandler_CreateInvoker.htm
tech.root: shell
ms.assetid: 12ffd2f1-e041-41f1-9b57-282a166ccbf7
ms.date: 12/05/2018
ms.keywords: CreateInvoker, CreateInvoker method [Windows Shell], CreateInvoker method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],CreateInvoker method, IAssocHandler.CreateInvoker, IAssocHandler::CreateInvoker, _shell_IAssocHandler_CreateInvoker, shell.IAssocHandler_CreateInvoker, shobjidl_core/IAssocHandler::CreateInvoker
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
 - IAssocHandler::CreateInvoker
 - shobjidl_core/IAssocHandler::CreateInvoker
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
 - IAssocHandler.CreateInvoker
---

# IAssocHandler::CreateInvoker


## -description

Retrieves an object that enables the invocation of the associated handler on the current selection.  The invoker includes the ability to verify whether the current selection is supported.

## -parameters

### -param pdo [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> that represents the selected item or items on which to invoke the handler. Note that if you have only a single item, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-invoke">IAssocHandler::Invoke</a> could be the better choice. See Remarks for more details.

### -param ppInvoker [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a>**</b>

When this method returns, contains the address of a pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a> object. This object is used to invoke the menu item after ensuring that the selected items are supported by the associated handler.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a> objects are typically used to populate an <b>Open With</b> menu. When one of those menu items is selected, this method is called to launch the chosen application.

<h3><a id="Invoke_and_CreateInvoker"></a><a id="invoke_and_createinvoker"></a><a id="INVOKE_AND_CREATEINVOKER"></a>Invoke and CreateInvoker</h3>
The <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> used by these methods can represent either a single file or it may represent a selection of multiple files. Not all applications support the multiple files option. Those applications that do support that scenario might impose other restrictions such as the number of files that can be opened at once, or acceptable combinations of file types.
              

Therefore, an application often must determine whether the handler supports the selection before trying to invoke the handler. For example, an application might enable a menu item only if it knew that the selection in question was supported by that handler.

It is generally safe to assume that an application will support invocation on a single item; in those cases the application typically calls <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-invoke">IAssocHandler::Invoke</a>.

For multiple selection scenarios, the application should call <b>IAssocHandler::CreateInvoker</b>. That method retrieves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker">IAssocHandlerInvoker</a> object that allows the calling application to first check whether the selection is supported (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandlerinvoker-supportsselection">SupportsSelection</a>), then to invoke the handler (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandlerinvoker-invoke">Invoke</a>).


<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-invoke">IAssocHandler::Invoke</a> can be called on a selection of multiple files, but it is not recommended due to the large processing load involved and no guarantee of success.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-invoke">IAssocHandler::Invoke</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers">IEnumAssocHandlers</a>
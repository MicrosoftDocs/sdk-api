---
UID: NF:shobjidl_core.IAssocHandler.CreateInvoker
title: IAssocHandler::CreateInvoker
author: windows-sdk-content
description: Retrieves an object that enables the invocation of the associated handler on the current selection. The invoker includes the ability to verify whether the current selection is supported.
old-location: shell\IAssocHandler_CreateInvoker.htm
old-project: shell
ms.assetid: 12ffd2f1-e041-41f1-9b57-282a166ccbf7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateInvoker, CreateInvoker method [Windows Shell], CreateInvoker method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],CreateInvoker method, IAssocHandler.CreateInvoker, IAssocHandler::CreateInvoker, _shell_IAssocHandler_CreateInvoker, shell.IAssocHandler_CreateInvoker, shobjidl_core/IAssocHandler::CreateInvoker
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IAssocHandler.CreateInvoker
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandler::CreateInvoker


## -description


Retrieves an object that enables the invocation of the associated handler on the current selection.  The invoker includes the ability to verify whether the current selection is supported.


## -parameters




### -param pdo [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> that represents the selected item or items on which to invoke the handler. Note that if you have only a single item, <a href="https://msdn.microsoft.com/2d22c987-3a25-4a36-8411-eaed921d066e">IAssocHandler::Invoke</a> could be the better choice. See Remarks for more details.


### -param ppInvoker [out]

Type: <b><a href="https://msdn.microsoft.com/b602280e-4237-4539-9a10-cec21c65e90d">IAssocHandlerInvoker</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/b602280e-4237-4539-9a10-cec21c65e90d">IAssocHandlerInvoker</a> object. This object is used to invoke the menu item after ensuring that the selected items are supported by the associated handler.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a> objects are typically used to populate an <b>Open With</b> menu. When one of those menu items is selected, this method is called to launch the chosen application.

<h3><a id="Invoke_and_CreateInvoker"></a><a id="invoke_and_createinvoker"></a><a id="INVOKE_AND_CREATEINVOKER"></a>Invoke and CreateInvoker</h3>

                The <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> used by these methods can represent either a single file or it may represent a selection of multiple files. Not all applications support the multiple files option. Those applications that do support that scenario might impose other restrictions such as the number of files that can be opened at once, or acceptable combinations of file types.
              

Therefore, an application often must determine whether the handler supports the selection before trying to invoke the handler. For example, an application might enable a menu item only if it knew that the selection in question was supported by that handler.

It is generally safe to assume that an application will support invocation on a single item; in those cases the application typically calls <a href="https://msdn.microsoft.com/2d22c987-3a25-4a36-8411-eaed921d066e">IAssocHandler::Invoke</a>.

For multiple selection scenarios, the application should call <b>IAssocHandler::CreateInvoker</b>. That method retrieves an <a href="https://msdn.microsoft.com/b602280e-4237-4539-9a10-cec21c65e90d">IAssocHandlerInvoker</a> object that allows the calling application to first check whether the selection is supported (<a href="https://msdn.microsoft.com/a4000557-2a89-494c-8b0e-c67a2e2c4445">SupportsSelection</a>), then to invoke the handler (<a href="https://msdn.microsoft.com/9b5de945-b177-4cbc-817c-447b2174323e">Invoke</a>).


<a href="https://msdn.microsoft.com/2d22c987-3a25-4a36-8411-eaed921d066e">IAssocHandler::Invoke</a> can be called on a selection of multiple files, but it is not recommended due to the large processing load involved and no guarantee of success.




## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/2d22c987-3a25-4a36-8411-eaed921d066e">IAssocHandler::Invoke</a>



<a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a>
 

 


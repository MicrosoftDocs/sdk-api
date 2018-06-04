---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


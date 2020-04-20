---
UID: NF:indexsrv.ISimpleCommandCreator.CreateICommand
title: ISimpleCommandCreator::CreateICommand (indexsrv.h)
description: Creates an ICommand.helpviewer_keywords: ["CreateICommand","CreateICommand method [search]","CreateICommand method [search]","ISimpleCommandCreator interface","ISimpleCommandCreator interface [search]","CreateICommand method","ISimpleCommandCreator.CreateICommand","ISimpleCommandCreator::CreateICommand","indexsrv/ISimpleCommandCreator::CreateICommand","search.isimplecommandcreator_createicommand"]
old-location: search\isimplecommandcreator_createicommand.htm
tech.root: search
ms.assetid: 70880905-E4DF-4064-A877-18AF5CE839FB
ms.date: 12/05/2018
ms.keywords: CreateICommand, CreateICommand method [search], CreateICommand method [search],ISimpleCommandCreator interface, ISimpleCommandCreator interface [search],CreateICommand method, ISimpleCommandCreator.CreateICommand, ISimpleCommandCreator::CreateICommand, indexsrv/ISimpleCommandCreator::CreateICommand, search.isimplecommandcreator_createicommand
f1_keywords:
- indexsrv/ISimpleCommandCreator.CreateICommand
dev_langs:
- c++
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Indexsrv.h
api_name:
- ISimpleCommandCreator.CreateICommand
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
---

# ISimpleCommandCreator::CreateICommand


## -description


Creates an ICommand.


## -parameters




### -param ppIUnknown

Returns the IUnknown for the command.


### -param pOuterUnk

Optional outer unknown pointer.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-isimplecommandcreator">ISimpleCommandCreator</a>
 

 


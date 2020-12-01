---
UID: NF:comsvcs.ISelectCOMLBServer.GetLBServer
title: ISelectCOMLBServer::GetLBServer (comsvcs.h)
description: Retrieves the name of the load balancing server.
helpviewer_keywords: ["GetLBServer","GetLBServer method [COM+]","GetLBServer method [COM+]","ISelectCOMLBServer interface","ISelectCOMLBServer interface [COM+]","GetLBServer method","ISelectCOMLBServer.GetLBServer","ISelectCOMLBServer::GetLBServer","_cos_ISelectCOMLBServer_GetLBServer","comsvcs/ISelectCOMLBServer::GetLBServer","cos.iselectcomlbserver_getlbserver"]
old-location: cos\iselectcomlbserver_getlbserver.htm
tech.root: cos
ms.assetid: 90b33e42-b26f-4dd8-bd91-939f452b7872
ms.date: 12/05/2018
ms.keywords: GetLBServer, GetLBServer method [COM+], GetLBServer method [COM+],ISelectCOMLBServer interface, ISelectCOMLBServer interface [COM+],GetLBServer method, ISelectCOMLBServer.GetLBServer, ISelectCOMLBServer::GetLBServer, _cos_ISelectCOMLBServer_GetLBServer, comsvcs/ISelectCOMLBServer::GetLBServer, cos.iselectcomlbserver_getlbserver
req.header: comsvcs.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISelectCOMLBServer::GetLBServer
 - comsvcs/ISelectCOMLBServer::GetLBServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISelectCOMLBServer.GetLBServer
---

# ISelectCOMLBServer::GetLBServer


## -description

Retrieves the name of  the load balancing server.

## -parameters

### -param pUnk [in, out]

A pointer to the load balancing server's name.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomlbarguments">ICOMLBArguments</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iselectcomlbserver">ISelectCOMLBServer</a>
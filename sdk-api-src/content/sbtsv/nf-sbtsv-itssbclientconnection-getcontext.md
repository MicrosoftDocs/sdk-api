---
UID: NF:sbtsv.ITsSbClientConnection.GetContext
title: ITsSbClientConnection::GetContext
author: windows-sdk-content
description: Retrieves context information that was stored by a plug-in by using the PutContext method.
old-location: termserv\itssbclientconnection_getcontext.htm
tech.root: TermServ
ms.assetid: dd4938b5-aa33-4eca-851c-fdef75ecc815
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetContext, GetContext method [Remote Desktop Services], GetContext method [Remote Desktop Services],ITsSbClientConnection interface, ITsSbClientConnection interface [Remote Desktop Services],GetContext method, ITsSbClientConnection.GetContext, ITsSbClientConnection::GetContext, sbtsv/ITsSbClientConnection::GetContext, termserv.itssbclientconnection_getcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - sbtsv.h
api_name:
 - ITsSbClientConnection.GetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbClientConnection::GetContext


## -description


Retrieves context information that was stored by a plug-in by using the <a href="https://msdn.microsoft.com/654714ef-cc86-41e8-8759-bbb66bd61cd2">PutContext</a> method.


## -parameters




### -param contextId [in]

A <b>BSTR</b> variable that contains the context ID.


### -param context [out, retval]

A pointer to the context information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/654714ef-cc86-41e8-8759-bbb66bd61cd2">PutContext</a>
 

 


---
UID: NF:objidlbase.ICancelMethodCalls.TestCancel
title: ICancelMethodCalls::TestCancel
author: windows-sdk-content
description: Determines whether a call has been canceled.
old-location: com\icancelmethodcalls_testcancel.htm
old-project: com
ms.assetid: 31141d97-241e-4717-b707-e37d86c2267d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICancelMethodCalls interface [COM],TestCancel method, ICancelMethodCalls.TestCancel, ICancelMethodCalls::TestCancel, TestCancel, TestCancel method [COM], TestCancel method [COM],ICancelMethodCalls interface, _com_icancelmethodcalls_testcancel, com.icancelmethodcalls_testcancel, objidlbase/ICancelMethodCalls::TestCancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ICancelMethodCalls.TestCancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICancelMethodCalls::TestCancel


## -description


Determines whether a call has been canceled.


## -parameters






## -returns



If the call was canceled, the return value is RPC_E_CALL_CANCELED. Otherwise, it is RPC_S_CALLPENDING.




## -remarks



The server object calls <b>TestCancel</b> to determine if the call has been canceled. If the call has been canceled, the server should clean up the necessary resources and return control to the client.

This method can be called from both the client and the server.




## -see-also




<a href="https://msdn.microsoft.com/9432621a-be31-4b8b-83b6-069539ba06b4">CoTestCancel</a>



<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 


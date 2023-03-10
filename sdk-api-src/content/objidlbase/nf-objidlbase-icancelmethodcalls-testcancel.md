---
UID: NF:objidlbase.ICancelMethodCalls.TestCancel
title: ICancelMethodCalls::TestCancel (objidlbase.h)
description: The ICancelMethodCalls::TestCancel (objidlbase.h) method determines whether a call has been canceled.
helpviewer_keywords: ["ICancelMethodCalls interface [COM]","TestCancel method","ICancelMethodCalls.TestCancel","ICancelMethodCalls::TestCancel","TestCancel","TestCancel method [COM]","TestCancel method [COM]","ICancelMethodCalls interface","_com_icancelmethodcalls_testcancel","com.icancelmethodcalls_testcancel","objidlbase/ICancelMethodCalls::TestCancel"]
old-location: com\icancelmethodcalls_testcancel.htm
tech.root: com
ms.assetid: 31141d97-241e-4717-b707-e37d86c2267d
ms.date: 08/13/2022
ms.keywords: ICancelMethodCalls interface [COM],TestCancel method, ICancelMethodCalls.TestCancel, ICancelMethodCalls::TestCancel, TestCancel, TestCancel method [COM], TestCancel method [COM],ICancelMethodCalls interface, _com_icancelmethodcalls_testcancel, com.icancelmethodcalls_testcancel, objidlbase/ICancelMethodCalls::TestCancel
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICancelMethodCalls::TestCancel
 - objidlbase/ICancelMethodCalls::TestCancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ICancelMethodCalls.TestCancel
---

# ICancelMethodCalls::TestCancel


## -description

Determines whether a call has been canceled.



## -returns

If the call was canceled, the return value is RPC_E_CALL_CANCELED. Otherwise, it is RPC_S_CALLPENDING.

## -remarks

The server object calls <b>TestCancel</b> to determine if the call has been canceled. If the call has been canceled, the server should clean up the necessary resources and return control to the client.

This method can be called from both the client and the server.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel">CoTestCancel</a>



<a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>

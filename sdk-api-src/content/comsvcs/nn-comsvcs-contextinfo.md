---
UID: NN:comsvcs.ContextInfo
title: ContextInfo (comsvcs.h)
description: Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.
helpviewer_keywords: ["ContextInfo","ContextInfo interface [COM+]","ContextInfo interface [COM+]","described","_cos_ContextInfo","comsvcs/ContextInfo","cos.contextinfo"]
old-location: cos\contextinfo.htm
tech.root: cos
ms.assetid: ef8d7ef7-fae4-4a20-80fb-18f5daa9b564
ms.date: 12/05/2018
ms.keywords: ContextInfo, ContextInfo interface [COM+], ContextInfo interface [COM+],described, _cos_ContextInfo, comsvcs/ContextInfo, cos.contextinfo
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
 - ContextInfo
 - comsvcs/ContextInfo
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
 - ContextInfo
---

# ContextInfo interface


## -description

Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

<b>ContextInfo</b> and <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a> provide the same functionality, but unlike <b>IObjectContextInfo</b>, <b>ContextInfo</b> is compatible with Automation.

In COM+ 1.5, released with Windows XP, the <b>ContextInfo</b> interface is superseded by the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo2">ContextInfo2</a> interface.

## -inheritance

The <b>ContextInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ContextInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>

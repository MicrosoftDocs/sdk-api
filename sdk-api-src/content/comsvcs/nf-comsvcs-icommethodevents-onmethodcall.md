---
UID: NF:comsvcs.IComMethodEvents.OnMethodCall
title: IComMethodEvents::OnMethodCall (comsvcs.h)
author: windows-sdk-content
description: Generated when an object's method is called.
old-location: cos\icommethodevents_onmethodcall.htm
tech.root: cossdk
ms.assetid: 5d68fe2c-7032-46d2-b88d-0b4f81c74760
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComMethodEvents interface [COM+],OnMethodCall method, IComMethodEvents.OnMethodCall, IComMethodEvents::OnMethodCall, OnMethodCall, OnMethodCall method [COM+], OnMethodCall method [COM+],IComMethodEvents interface, _dtc_IComMethodEvents_OnMethodCall, comsvcs/IComMethodEvents::OnMethodCall, cos.icommethodevents_onmethodcall
ms.topic: method
f1_keywords: ["comsvcs/IComMethodEvents.OnMethodCall"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComMethodEvents.OnMethodCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComMethodEvents::OnMethodCall


## -description


Generated when an object's method is called.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param oid [in]

The just-in-time (JIT) activated object.


### -param guidCid [in]

The CLSID for the object being called.


### -param guidRid [in]

The identifier of the method being called.


### -param iMeth [in]

The v-table index of the method.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a>
 

 


---
UID: NF:comsvcs.GetManagedExtensions
title: GetManagedExtensions function (comsvcs.h)
description: Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).
helpviewer_keywords: ["GetManagedExtensions","GetManagedExtensions function [COM+]","_cos_GetManagedExtensions","comsvcs/GetManagedExtensions","cos.getmanagedextensions"]
old-location: cos\getmanagedextensions.htm
tech.root: cos
ms.assetid: cffd18c4-6e37-447b-b749-64793711ea56
ms.date: 12/05/2018
ms.keywords: GetManagedExtensions, GetManagedExtensions function [COM+], _cos_GetManagedExtensions, comsvcs/GetManagedExtensions, cos.getmanagedextensions
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetManagedExtensions
 - comsvcs/GetManagedExtensions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - GetManagedExtensions
---

# GetManagedExtensions function


## -description

Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).

## -parameters

### -param dwExts [out]

Indicates whether the installed version of COM+ supports managed extensions. A value of 1 indicates that it does, while a value of 0 indicates that it does not.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Several COM+ services, such as <a href="/windows/desktop/cossdk/com--just-in-time-activation">COM+ Just-in-Time Activation</a> and <a href="/windows/desktop/cossdk/com--events">COM+ Events</a>, support the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedactivationevents">IManagedActivationEvents</a> interface. This interface provides additional code for managing serviced components (managed objects). To take advantage of this additional code, the serviced component must support the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a> interface. The <b>GetManagedExtensions</b> function allows you to determine the availability of this additional code in the installed version of COM+.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedactivationevents">IManagedActivationEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a>
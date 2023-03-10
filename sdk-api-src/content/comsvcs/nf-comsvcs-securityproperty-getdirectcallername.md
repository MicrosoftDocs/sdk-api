---
UID: NF:comsvcs.SecurityProperty.GetDirectCallerName
title: SecurityProperty::GetDirectCallerName (comsvcs.h)
description: Retrieves the user name associated with the external process that called the currently executing method.
helpviewer_keywords: ["GetDirectCallerName","GetDirectCallerName method [COM+]","GetDirectCallerName method [COM+]","SecurityProperty interface","SecurityProperty interface [COM+]","GetDirectCallerName method","SecurityProperty.GetDirectCallerName","SecurityProperty::GetDirectCallerName","_cos_SecurityProperty_GetDirectCallerName","comsvcs/SecurityProperty::GetDirectCallerName","cos.securityproperty_getdirectcallername"]
old-location: cos\securityproperty_getdirectcallername.htm
tech.root: cos
ms.assetid: 451e073f-8dba-459a-92f3-4e9f1128a2c6
ms.date: 12/05/2018
ms.keywords: GetDirectCallerName, GetDirectCallerName method [COM+], GetDirectCallerName method [COM+],SecurityProperty interface, SecurityProperty interface [COM+],GetDirectCallerName method, SecurityProperty.GetDirectCallerName, SecurityProperty::GetDirectCallerName, _cos_SecurityProperty_GetDirectCallerName, comsvcs/SecurityProperty::GetDirectCallerName, cos.securityproperty_getdirectcallername
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
 - SecurityProperty::GetDirectCallerName
 - comsvcs/SecurityProperty::GetDirectCallerName
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
 - SecurityProperty.GetDirectCallerName
---

# SecurityProperty::GetDirectCallerName


## -description

Retrieves the user name associated with the external process that called the currently executing method.

## -parameters

### -param bstrUserName [out]

A reference to the user name associated with the external process that called the currently executing method.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The following scenarios illustrate the functionality of this method:

<ul>
<li>A base process, running on server A as user A, calls into object X on server B, running as user B. Then object X calls into object Y, running on server C. If object Y calls <b>GetDirectCallerName</b>, the name of user B is retrieved.</li>
<li>A base process, running on server A as user A, calls into object X on server B, running as user B. Then object X calls into object Y, running in the same process as object X, also on server B. When object Y calls <b>GetDirectCallerName</b>, the name of user A is returned, not the name of user B.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-securityproperty">SecurityProperty</a>
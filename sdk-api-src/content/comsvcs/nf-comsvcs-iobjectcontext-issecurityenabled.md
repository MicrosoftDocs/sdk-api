---
UID: NF:comsvcs.IObjectContext.IsSecurityEnabled
title: IObjectContext::IsSecurityEnabled (comsvcs.h)
description: Indicates whether security is enabled for the current object. COM+ security is enabled unless the object is running in the client's process.
helpviewer_keywords: ["IObjectContext interface [COM+]","IsSecurityEnabled method","IObjectContext.IsSecurityEnabled","IObjectContext::IsSecurityEnabled","IsSecurityEnabled","IsSecurityEnabled method [COM+]","IsSecurityEnabled method [COM+]","IObjectContext interface","_cos_IObjectContext_IsSecurityEnabled","comsvcs/IObjectContext::IsSecurityEnabled","cos.iobjectcontext_issecurityenabled"]
old-location: cos\iobjectcontext_issecurityenabled.htm
tech.root: cos
ms.assetid: eba720e5-5c25-4723-b9e5-3bbdb69ada30
ms.date: 12/05/2018
ms.keywords: IObjectContext interface [COM+],IsSecurityEnabled method, IObjectContext.IsSecurityEnabled, IObjectContext::IsSecurityEnabled, IsSecurityEnabled, IsSecurityEnabled method [COM+], IsSecurityEnabled method [COM+],IObjectContext interface, _cos_IObjectContext_IsSecurityEnabled, comsvcs/IObjectContext::IsSecurityEnabled, cos.iobjectcontext_issecurityenabled
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
 - IObjectContext::IsSecurityEnabled
 - comsvcs/IObjectContext::IsSecurityEnabled
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
 - IObjectContext.IsSecurityEnabled
---

# IObjectContext::IsSecurityEnabled


## -description

Indicates whether security is enabled for the current object. COM+ security is enabled unless the object is running in the client's process.



## -returns

If security is enabled for this object, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -remarks

In the COM+ environment, server and library applications can use role-based security. <b>IsSecurityEnabled</b> returns <b>TRUE</b> when an application uses role-based security, and role-based security is enabled both for the application and the specific component that called the method. 

<b>MTS 2.0:  </b>In MTS 2.0, this method always returns <b>FALSE</b> when the current object is running in a library application, because MTS library applications cannot use role-based security. However, in the COM+ environment, library applications optionally can use role-based security.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>

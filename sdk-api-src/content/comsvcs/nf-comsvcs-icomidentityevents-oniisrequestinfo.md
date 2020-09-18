---
UID: NF:comsvcs.IComIdentityEvents.OnIISRequestInfo
title: IComIdentityEvents::OnIISRequestInfo (comsvcs.h)
description: Generated when an activity is part of an ASP page.
helpviewer_keywords: ["IComIdentityEvents interface [COM+]","OnIISRequestInfo method","IComIdentityEvents.OnIISRequestInfo","IComIdentityEvents::OnIISRequestInfo","OnIISRequestInfo","OnIISRequestInfo method [COM+]","OnIISRequestInfo method [COM+]","IComIdentityEvents interface","_dtc_IComIdentityEvents_OnIISRequestInfo","comsvcs/IComIdentityEvents::OnIISRequestInfo","cos.icomidentityevents_oniisrequestinfo"]
old-location: cos\icomidentityevents_oniisrequestinfo.htm
tech.root: cos
ms.assetid: 88beaef9-d042-4836-8223-6063c87ba06a
ms.date: 12/05/2018
ms.keywords: IComIdentityEvents interface [COM+],OnIISRequestInfo method, IComIdentityEvents.OnIISRequestInfo, IComIdentityEvents::OnIISRequestInfo, OnIISRequestInfo, OnIISRequestInfo method [COM+], OnIISRequestInfo method [COM+],IComIdentityEvents interface, _dtc_IComIdentityEvents_OnIISRequestInfo, comsvcs/IComIdentityEvents::OnIISRequestInfo, cos.icomidentityevents_oniisrequestinfo
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
 - IComIdentityEvents::OnIISRequestInfo
 - comsvcs/IComIdentityEvents::OnIISRequestInfo
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
 - IComIdentityEvents.OnIISRequestInfo
---

# IComIdentityEvents::OnIISRequestInfo


## -description

Generated when an activity is part of an ASP page.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param ObjId [in]

The unique identifier for this object.

### -param pszClientIP [in]

The Internet Protocol (IP) address of the IIS client.

### -param pszServerIP [in]

The IP address of the IIS server.

### -param pszURL [in]

The URL on IIS server generating object reference.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomidentityevents">IComIdentityEvents</a>
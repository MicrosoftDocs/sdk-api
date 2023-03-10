---
UID: NN:azroles.IAzApplication
title: IAzApplication (azroles.h)
description: Defines an installed instance of an application. An IAzApplication object is created when an application is installed.
helpviewer_keywords: ["IAzApplication","IAzApplication interface [Security]","IAzApplication interface [Security]","described","azroles/IAzApplication","security.iazapplication"]
old-location: security\iazapplication.htm
tech.root: security
ms.assetid: ea4a8a84-5003-44da-b75e-34da6bd898dd
ms.date: 12/05/2018
ms.keywords: IAzApplication, IAzApplication interface [Security], IAzApplication interface [Security],described, azroles/IAzApplication, security.iazapplication
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication
 - azroles/IAzApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication
---

# IAzApplication interface


## -description

The <b>IAzApplication</b> interface defines an installed instance of an application. An <b>IAzApplication</b> object is created when an application is installed.

## -inheritance

The <b>IAzApplication</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzApplication</b> also has these types of members:

## -remarks

The <b>IAzApplication</b> object is a container in which all authorization policies that apply to an instance of an application reside.

## -see-also

<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Allowing Anonymous Access</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

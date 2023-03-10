---
UID: NN:azroles.IAzScope
title: IAzScope (azroles.h)
description: Defines a logical container of resources to which the application manages access.
helpviewer_keywords: ["IAzScope","IAzScope interface [Security]","IAzScope interface [Security]","described","azroles/IAzScope","security.iazscope"]
old-location: security\iazscope.htm
tech.root: security
ms.assetid: f7abe7cb-8827-46f6-85fe-99282582a3d4
ms.date: 12/05/2018
ms.keywords: IAzScope, IAzScope interface [Security], IAzScope interface [Security],described, azroles/IAzScope, security.iazscope
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
 - IAzScope
 - azroles/IAzScope
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
 - IAzScope
---

# IAzScope interface


## -description

The <b>IAzScope</b> interface defines a logical container of resources to which the application manages access. The scope name will be used in calls to the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method to determine whether a user has the requested access to resources logically contained within the scope.

## -inheritance

The <b>IAzScope</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzScope</b> also has these types of members:


---
UID: NN:azroles.IAzRoleAssignment
title: IAzRoleAssignment (azroles.h)
description: Represents a role to which users and groups can be assigned.
helpviewer_keywords: ["IAzRoleAssignment","IAzRoleAssignment interface [Security]","IAzRoleAssignment interface [Security]","described","azroles/IAzRoleAssignment","security.iazroleassignment"]
old-location: security\iazroleassignment.htm
tech.root: security
ms.assetid: 3f0b926f-77f4-4477-b155-5f866822baba
ms.date: 12/05/2018
ms.keywords: IAzRoleAssignment, IAzRoleAssignment interface [Security], IAzRoleAssignment interface [Security],described, azroles/IAzRoleAssignment, security.iazroleassignment
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzRoleAssignment
 - azroles/IAzRoleAssignment
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
 - IAzRoleAssignment
---

# IAzRoleAssignment interface


## -description

The <b>IAzRoleAssignment</b> interface represents a role to which users and groups can be assigned. A <b>IAzRoleAssignment</b> object can be associated with one or more <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a>, <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>, and <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects that specify the operations to which users and groups assigned to the role can access.

## -inheritance

The <b>IAzRoleAssignment</b> interface inherits from <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a>. <b>IAzRoleAssignment</b> also has these types of members:


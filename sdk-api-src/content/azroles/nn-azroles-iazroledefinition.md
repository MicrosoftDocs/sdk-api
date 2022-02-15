---
UID: NN:azroles.IAzRoleDefinition
title: IAzRoleDefinition (azroles.h)
description: Represents one or more IAzRoleDefinition, IAzTask, and IAzOperation objects that specify a set of operations.
helpviewer_keywords: ["IAzRoleDefinition","IAzRoleDefinition interface [Security]","IAzRoleDefinition interface [Security]","described","azroles/IAzRoleDefinition","security.iazroledefinition"]
old-location: security\iazroledefinition.htm
tech.root: security
ms.assetid: d951f5cc-85da-4898-a70f-9e50ab66ade5
ms.date: 12/05/2018
ms.keywords: IAzRoleDefinition, IAzRoleDefinition interface [Security], IAzRoleDefinition interface [Security],described, azroles/IAzRoleDefinition, security.iazroledefinition
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
 - IAzRoleDefinition
 - azroles/IAzRoleDefinition
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
 - IAzRoleDefinition
---

# IAzRoleDefinition interface


## -description

The <b>IAzRoleDefinition</b> interface represents one or more <b>IAzRoleDefinition</b>, <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>, and <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects that specify a set of operations. If an <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object is associated with an <b>IAzRoleDefinition</b> object, users and groups assigned to that <b>IAzRoleAssignment</b> object are allowed to access the operations specified by that <b>IAzRoleDefinition</b> object.

## -inheritance

The <b>IAzRoleDefinition</b> interface inherits from <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>. <b>IAzRoleDefinition</b> also has these types of members:


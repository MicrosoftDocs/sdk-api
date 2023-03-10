---
UID: NF:comsvcs.SecurityProperty.GetOriginalCreatorName
title: SecurityProperty::GetOriginalCreatorName (comsvcs.h)
description: Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.
helpviewer_keywords: ["GetOriginalCreatorName","GetOriginalCreatorName method [COM+]","GetOriginalCreatorName method [COM+]","SecurityProperty interface","SecurityProperty interface [COM+]","GetOriginalCreatorName method","SecurityProperty.GetOriginalCreatorName","SecurityProperty::GetOriginalCreatorName","_cos_SecurityProperty_GetOriginalCreatorName","comsvcs/SecurityProperty::GetOriginalCreatorName","cos.securityproperty_getoriginalcreatorname"]
old-location: cos\securityproperty_getoriginalcreatorname.htm
tech.root: cos
ms.assetid: 403f0f36-f386-4eeb-905a-e04c5699db9b
ms.date: 12/05/2018
ms.keywords: GetOriginalCreatorName, GetOriginalCreatorName method [COM+], GetOriginalCreatorName method [COM+],SecurityProperty interface, SecurityProperty interface [COM+],GetOriginalCreatorName method, SecurityProperty.GetOriginalCreatorName, SecurityProperty::GetOriginalCreatorName, _cos_SecurityProperty_GetOriginalCreatorName, comsvcs/SecurityProperty::GetOriginalCreatorName, cos.securityproperty_getoriginalcreatorname
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
 - SecurityProperty::GetOriginalCreatorName
 - comsvcs/SecurityProperty::GetOriginalCreatorName
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
 - SecurityProperty.GetOriginalCreatorName
---

# SecurityProperty::GetOriginalCreatorName


## -description

<p class="CCE_Message">[Do not use this method in COM+ applications because it was designed to be used only in MTS 2.0 applications.]

Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.

## -parameters

### -param bstrUserName [out]

A reference to the user name associated with the original base process that initiated the activity in which the current object is executing.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-securityproperty">SecurityProperty</a>
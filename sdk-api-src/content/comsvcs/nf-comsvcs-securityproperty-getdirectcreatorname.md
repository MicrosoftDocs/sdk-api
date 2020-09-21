---
UID: NF:comsvcs.SecurityProperty.GetDirectCreatorName
title: SecurityProperty::GetDirectCreatorName (comsvcs.h)
description: Retrieves the user name associated with the current object's immediate (out-of-process) creator.
helpviewer_keywords: ["GetDirectCreatorName","GetDirectCreatorName method [COM+]","GetDirectCreatorName method [COM+]","SecurityProperty interface","SecurityProperty interface [COM+]","GetDirectCreatorName method","SecurityProperty.GetDirectCreatorName","SecurityProperty::GetDirectCreatorName","_cos_SecurityProperty_GetDirectCreatorName","comsvcs/SecurityProperty::GetDirectCreatorName","cos.securityproperty_getdirectcreatorname"]
old-location: cos\securityproperty_getdirectcreatorname.htm
tech.root: cos
ms.assetid: 26619719-bcca-4776-9580-edc541e6b821
ms.date: 12/05/2018
ms.keywords: GetDirectCreatorName, GetDirectCreatorName method [COM+], GetDirectCreatorName method [COM+],SecurityProperty interface, SecurityProperty interface [COM+],GetDirectCreatorName method, SecurityProperty.GetDirectCreatorName, SecurityProperty::GetDirectCreatorName, _cos_SecurityProperty_GetDirectCreatorName, comsvcs/SecurityProperty::GetDirectCreatorName, cos.securityproperty_getdirectcreatorname
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
 - SecurityProperty::GetDirectCreatorName
 - comsvcs/SecurityProperty::GetDirectCreatorName
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
 - SecurityProperty.GetDirectCreatorName
---

# SecurityProperty::GetDirectCreatorName


## -description

<p class="CCE_Message">[Do not use this method in COM+ applications because it was designed to be used only in MTS 2.0 applications.]

Retrieves the user name associated with the current object's immediate (out-of-process) creator.

## -parameters

### -param bstrUserName [out]

A reference to the user name associated with the current object's immediate (out-of-process) creator.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-securityproperty">SecurityProperty</a>
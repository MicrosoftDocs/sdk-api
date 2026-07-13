---
UID: NE:certenroll.PolicyServerUrlPropertyID
title: PolicyServerUrlPropertyID (certenroll.h)
description: Contains values that specify the type of property value to be returned by the GetStringProperty method or set by the SetStringProperty method on the IX509PolicyServerUrl interface.
helpviewer_keywords: ["PolicyServerUrlPropertyID","PolicyServerUrlPropertyID enumeration [Security]","PsFriendlyName","PsPolicyID","certenroll/PolicyServerUrlPropertyID","certenroll/PsFriendlyName","certenroll/PsPolicyID","security.policyserverurlpropertyid"]
old-location: security\policyserverurlpropertyid.htm
tech.root: security
ms.assetid: 7b2f898d-9730-4f86-a7b2-dd625889c00a
ms.date: 12/05/2018
ms.keywords: PolicyServerUrlPropertyID, PolicyServerUrlPropertyID enumeration [Security], PsFriendlyName, PsPolicyID, certenroll/PolicyServerUrlPropertyID, certenroll/PsFriendlyName, certenroll/PsPolicyID, security.policyserverurlpropertyid
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PolicyServerUrlPropertyID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PolicyServerUrlPropertyID
 - certenroll/PolicyServerUrlPropertyID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certenroll.h
api_name:
 - PolicyServerUrlPropertyID
---

# PolicyServerUrlPropertyID enumeration


## -description

The <b>PolicyServerUrlPropertyID</b> enumeration contains values that specify the type of property value to be returned by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509policyserverurl-getstringproperty">GetStringProperty</a> method or set by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509policyserverurl-setstringproperty">SetStringProperty</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> interface.

## -enum-fields

### -field PsPolicyID:0

Specify or retrieve an ID for the policy server.

### -field PsFriendlyName:1

Specify or retrieve a display name for the policy server.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509policyserverurl-getstringproperty">GetStringProperty</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509policyserverurl-setstringproperty">SetStringProperty</a>

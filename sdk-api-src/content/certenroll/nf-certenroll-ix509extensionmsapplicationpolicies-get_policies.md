---
UID: NF:certenroll.IX509ExtensionMSApplicationPolicies.get_Policies
title: IX509ExtensionMSApplicationPolicies::get_Policies (certenroll.h)
description: Retrieves a collection of application policies.
helpviewer_keywords: ["IX509ExtensionMSApplicationPolicies interface [Security]","Policies property","IX509ExtensionMSApplicationPolicies.Policies","IX509ExtensionMSApplicationPolicies.get_Policies","IX509ExtensionMSApplicationPolicies::Policies","IX509ExtensionMSApplicationPolicies::get_Policies","Policies property [Security]","Policies property [Security]","IX509ExtensionMSApplicationPolicies interface","certenroll/IX509ExtensionMSApplicationPolicies::Policies","certenroll/IX509ExtensionMSApplicationPolicies::get_Policies","get_Policies","security.ix509extensionmsapplicationpolicies_policies_property"]
old-location: security\ix509extensionmsapplicationpolicies_policies_property.htm
tech.root: security
ms.assetid: e20c7e75-ec08-4336-b932-f0bb0a5dfee8
ms.date: 12/05/2018
ms.keywords: IX509ExtensionMSApplicationPolicies interface [Security],Policies property, IX509ExtensionMSApplicationPolicies.Policies, IX509ExtensionMSApplicationPolicies.get_Policies, IX509ExtensionMSApplicationPolicies::Policies, IX509ExtensionMSApplicationPolicies::get_Policies, Policies property [Security], Policies property [Security],IX509ExtensionMSApplicationPolicies interface, certenroll/IX509ExtensionMSApplicationPolicies::Policies, certenroll/IX509ExtensionMSApplicationPolicies::get_Policies, get_Policies, security.ix509extensionmsapplicationpolicies_policies_property
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509ExtensionMSApplicationPolicies::get_Policies
 - certenroll/IX509ExtensionMSApplicationPolicies::get_Policies
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509ExtensionMSApplicationPolicies.Policies
 - IX509ExtensionMSApplicationPolicies.get_Policies
---

# IX509ExtensionMSApplicationPolicies::get_Policies


## -description

The <b>Policies</b> property retrieves a collection of application policies.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionmsapplicationpolicies-initializeencode">InitializeEncode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionmsapplicationpolicies-initializedecode">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a>
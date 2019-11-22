---
UID: NF:certenroll.IX509ExtensionBasicConstraints.get_PathLenConstraint
title: IX509ExtensionBasicConstraints::get_PathLenConstraint (certenroll.h)

description: Retrieves the depth of the subordinate certification authority chain.
old-location: security\ix509extensionbasicconstraints_pathlenconstraint_property.htm
tech.root: seccertenroll
ms.assetid: 6d688596-60fd-47d0-8f91-cfda448ac015

ms.date: 12/05/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],PathLenConstraint property, IX509ExtensionBasicConstraints.PathLenConstraint, IX509ExtensionBasicConstraints.get_PathLenConstraint, IX509ExtensionBasicConstraints::PathLenConstraint, IX509ExtensionBasicConstraints::get_PathLenConstraint, PathLenConstraint property [Security], PathLenConstraint property [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::PathLenConstraint, certenroll/IX509ExtensionBasicConstraints::get_PathLenConstraint, get_PathLenConstraint, security.ix509extensionbasicconstraints_pathlenconstraint_property
ms.topic: method
f1_keywords: 
 - "certenroll/IX509ExtensionBasicConstraints.PathLenConstraint"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509ExtensionBasicConstraints.PathLenConstraint
 - IX509ExtensionBasicConstraints.get_PathLenConstraint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionBasicConstraints::get_PathLenConstraint


## -description


The <b>PathLenConstraint</b> property retrieves the depth of the subordinate certification authority chain.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializeencode">InitializeEncode</a> method or the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializedecode">InitializeDecode</a> method to initialize the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a> object and specify the <b>PathLenConstraint</b> property. You can also call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a>
 

 


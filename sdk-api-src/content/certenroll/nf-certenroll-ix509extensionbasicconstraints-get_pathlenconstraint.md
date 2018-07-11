---
UID: NF:certenroll.IX509ExtensionBasicConstraints.get_PathLenConstraint
title: IX509ExtensionBasicConstraints::get_PathLenConstraint
author: windows-sdk-content
description: Retrieves the depth of the subordinate certification authority chain.
old-location: security\ix509extensionbasicconstraints_pathlenconstraint_property.htm
old-project: seccertenroll
ms.assetid: 6d688596-60fd-47d0-8f91-cfda448ac015
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],PathLenConstraint property, IX509ExtensionBasicConstraints.PathLenConstraint, IX509ExtensionBasicConstraints.get_PathLenConstraint, IX509ExtensionBasicConstraints::PathLenConstraint, IX509ExtensionBasicConstraints::get_PathLenConstraint, PathLenConstraint property [Security], PathLenConstraint property [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::PathLenConstraint, certenroll/IX509ExtensionBasicConstraints::get_PathLenConstraint, get_PathLenConstraint, security.ix509extensionbasicconstraints_pathlenconstraint_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: X509RequestType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionBasicConstraints::get_PathLenConstraint


## -description


The <b>PathLenConstraint</b> property retrieves the depth of the subordinate certification authority chain.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/e9a08445-8fc5-45cc-a2c6-ec62470e5c55">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/3b0b5547-6871-412a-8463-889af3b1302b">InitializeDecode</a> method to initialize the <a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a> object and specify the <b>PathLenConstraint</b> property. You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a>
 

 


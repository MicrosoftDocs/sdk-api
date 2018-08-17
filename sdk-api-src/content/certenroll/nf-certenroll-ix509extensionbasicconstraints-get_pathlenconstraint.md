---
UID: NF:certenroll.IX509ExtensionBasicConstraints.get_PathLenConstraint
title: IX509ExtensionBasicConstraints::get_PathLenConstraint
author: windows-sdk-content
description: Retrieves the depth of the subordinate certification authority chain.
old-location: security\ix509extensionbasicconstraints_pathlenconstraint_property.htm
old-project: seccertenroll
ms.assetid: 6d688596-60fd-47d0-8f91-cfda448ac015
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],PathLenConstraint property, IX509ExtensionBasicConstraints.PathLenConstraint, IX509ExtensionBasicConstraints.get_PathLenConstraint, IX509ExtensionBasicConstraints::PathLenConstraint, IX509ExtensionBasicConstraints::get_PathLenConstraint, PathLenConstraint property [Security], PathLenConstraint property [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::PathLenConstraint, certenroll/IX509ExtensionBasicConstraints::get_PathLenConstraint, get_PathLenConstraint, security.ix509extensionbasicconstraints_pathlenconstraint_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378112(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378109(v=VS.85).aspx">InitializeDecode</a> method to initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a> object and specify the <b>PathLenConstraint</b> property. You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a>
 

 


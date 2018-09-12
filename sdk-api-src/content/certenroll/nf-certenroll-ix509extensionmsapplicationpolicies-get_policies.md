---
UID: NF:certenroll.IX509ExtensionMSApplicationPolicies.get_Policies
title: IX509ExtensionMSApplicationPolicies::get_Policies
author: windows-sdk-content
description: Retrieves a collection of application policies.
old-location: security\ix509extensionmsapplicationpolicies_policies_property.htm
tech.root: SecCertEnroll
ms.assetid: e20c7e75-ec08-4336-b932-f0bb0a5dfee8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509ExtensionMSApplicationPolicies interface [Security],Policies property, IX509ExtensionMSApplicationPolicies.Policies, IX509ExtensionMSApplicationPolicies.get_Policies, IX509ExtensionMSApplicationPolicies::Policies, IX509ExtensionMSApplicationPolicies::get_Policies, Policies property [Security], Policies property [Security],IX509ExtensionMSApplicationPolicies interface, certenroll/IX509ExtensionMSApplicationPolicies::Policies, certenroll/IX509ExtensionMSApplicationPolicies::get_Policies, get_Policies, security.ix509extensionmsapplicationpolicies_policies_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IX509ExtensionMSApplicationPolicies.Policies
 - IX509ExtensionMSApplicationPolicies.get_Policies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionMSApplicationPolicies::get_Policies


## -description


The <b>Policies</b> property retrieves a collection of application policies.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378161(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378160(v=VS.85).aspx">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378155(v=VS.85).aspx">IX509ExtensionMSApplicationPolicies</a>
 

 


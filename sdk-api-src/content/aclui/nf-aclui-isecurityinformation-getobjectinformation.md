---
UID: NF:aclui.ISecurityInformation.GetObjectInformation
title: ISecurityInformation::GetObjectInformation
author: windows-sdk-content
description: The GetObjectInformation method requests information that the access control editor uses to initialize its pages and to determine the editing options available to the user.
old-location: security\isecurityinformation_getobjectinformation.htm
tech.root: secauthz
ms.assetid: 2bc63aa0-dada-4962-a381-6b0f8332e564
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetObjectInformation, GetObjectInformation method [Security], GetObjectInformation method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetObjectInformation method, ISecurityInformation.GetObjectInformation, ISecurityInformation::GetObjectInformation, _win32_isecurityinformation_getobjectinformation, aclui/ISecurityInformation::GetObjectInformation, security.isecurityinformation_getobjectinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.GetObjectInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::GetObjectInformation


## -description


The <b>GetObjectInformation</b> method requests information that the access control editor uses to initialize its pages and to determine the editing options available to the user.


## -parameters




### -param pObjectInfo [out]

A pointer to an 
<a href="https://msdn.microsoft.com/bdfd0753-4727-4ca1-ac36-0a77db0a16c5">SI_OBJECT_INFO</a> structure. Your implementation must fill this structure to pass information back to the access control editor.


## -returns



Returns S_OK if successful.

Returns a nonzero error code if an error occurs.




## -remarks



The system does not free the string pointers that you return in the 
<a href="https://msdn.microsoft.com/bdfd0753-4727-4ca1-ac36-0a77db0a16c5">SI_OBJECT_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/bdfd0753-4727-4ca1-ac36-0a77db0a16c5">SI_OBJECT_INFO</a>
 

 


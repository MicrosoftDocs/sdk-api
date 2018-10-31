---
UID: NF:aclui.ISecurityInformation2.IsDaclCanonical
title: ISecurityInformation2::IsDaclCanonical
author: windows-sdk-content
description: The IsDaclCanonical method determines whether the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.
old-location: security\isecurityinformation2_isdaclcanonical.htm
tech.root: secauthz
ms.assetid: 54b83592-0cfb-45db-9788-05459c9ec35c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ISecurityInformation2 interface [Security],IsDaclCanonical method, ISecurityInformation2.IsDaclCanonical, ISecurityInformation2::IsDaclCanonical, IsDaclCanonical, IsDaclCanonical method [Security], IsDaclCanonical method [Security],ISecurityInformation2 interface, _win32_isecurityinformation2_isdaclcanonical, aclui/ISecurityInformation2::IsDaclCanonical, security.isecurityinformation2_isdaclcanonical
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
 - ISecurityInformation2.IsDaclCanonical
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation2::IsDaclCanonical


## -description


The <b>IsDaclCanonical</b> method determines whether the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.


## -parameters




### -param pDacl [in]

A pointer to a discretionary 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure initialized by 
<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>.


## -returns



Returns <b>TRUE</b> if the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.

Returns <b>FALSE</b> if the ACEs are not ordered correctly.




## -remarks



If the return value of this method is <b>FALSE</b>, the access control editor  displays a message box stating that the DACL is incorrectly ordered. If this method is not provided and the editor requires this information, the editor will check the  canonical ordering defined in 
<a href="https://msdn.microsoft.com/fccf043e-e769-4f3f-b18c-252be20190d8">Order of ACEs in a DACL</a>.




## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>



<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>
 

 


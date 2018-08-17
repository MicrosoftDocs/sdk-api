---
UID: NF:aclui.EditSecurity
title: EditSecurity function
author: windows-sdk-content
description: Displays a property sheet that contains a basic security property page. This property page enables the user to view and edit the access rights allowed or denied by the ACEs in an object's DACL.
old-location: security\editsecurity.htm
old-project: secauthz
ms.assetid: 756c94b0-946f-47eb-b4b4-db3e6e89fe46
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: EditSecurity, EditSecurity function [Security], _win32_editsecurity, aclui/EditSecurity, security.editsecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclui.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SI_PAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Aclui.dll
api_name:
 - EditSecurity
product: Windows
targetos: Windows
req.lib: Aclui.lib
req.dll: Aclui.dll
req.irql: 
---

# EditSecurity function


## -description


The <b>EditSecurity</b> function displays a property sheet that contains a 
<a href="https://msdn.microsoft.com/6623fe7e-e91d-49c7-9ad0-7791c178d12b">basic security property page</a>. This property page enables the user to view and edit the access rights allowed or denied by the ACEs in an object's DACL.


## -parameters




### -param hwndOwner [in]

A handle to the window that owns the property sheet. This parameter can be <b>NULL</b>.


### -param psi [in]

A pointer to your implementation of the 
<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface. The system calls the interface methods to retrieve information about the object being edited and to return the user's input.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>EditSecurity</b> function calls the 
<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a> function to create a basic security property page.

During the property page initialization, the system calls the 
<a href="https://msdn.microsoft.com/4c9e05fd-0b58-4d6d-b33e-067d9e8e2915">ISecurityInformation::GetSecurity</a> and 
<a href="https://msdn.microsoft.com/7c23c5ad-8088-4cfb-9746-99d24cc3bd0e">ISecurityInformation::SetSecurity</a> methods to determine whether the user has permission to edit the object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. The system displays an error message if the user does not have permission.

The basic security property page can include an <b>Advanced</b> button for displaying the 
<a href="https://msdn.microsoft.com/99911751-d4ac-4325-89f5-23d237bfd428">advanced security property sheet</a>. This advanced security property sheet can contain three additional property pages that enable the user to view and edit the object's DACL, SACL, and owner.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/4c9e05fd-0b58-4d6d-b33e-067d9e8e2915">GetSecurity</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/7c23c5ad-8088-4cfb-9746-99d24cc3bd0e">SetSecurity</a>
 

 


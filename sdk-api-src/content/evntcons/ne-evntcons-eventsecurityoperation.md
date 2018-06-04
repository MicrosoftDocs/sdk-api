---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EVENTSECURITYOPERATION enumeration


## -description


Defines what component of the security descriptor that the <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a> function modifies.


## -enum-fields




### -field EventSecuritySetDACL

Clears the current discretionary access control list (DACL) and adds an ACE to the DACL. The <i>Sid</i>, <i>Rights</i>, and <i>AllowOrDeny</i> parameters of the <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a> function determine the contents of the ACE (who has access to the provider or session and the type of access). To add a new ACE to the DACL without clearing the existing DACL, specify EventSecurityAddDACL.


### -field EventSecuritySetSACL

Clears the current system access control list (SACL) and adds an audit ACE to the SACL. The <i>Sid</i> and <i>Rights</i> parameters of the <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a> function determine the contents of the ACE (who generates an audit record when attempting the specified access). To add a new ACE to the SACL without clearing the existing SACL, specify EventSecurityAddSACL.


### -field EventSecurityAddDACL

Adds an ACE to the current DACL. The <i>Sid</i>, <i>Rights</i>, and <i>AllowOrDeny</i> parameters of the <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a> function determine the contents of the ACE (who has access to the provider or session and the type of access). 


### -field EventSecurityAddSACL

Adds an ACE to the current SACL. The <i>Sid</i> and <i>Rights</i> parameters of the <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a> function determine the contents of the ACE (who generates an audit record when attempting the specified access).


### -field EventSecurityMax

Reserved.


## -remarks



For information on DACLs and SACLs, see <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">Access Control Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>
 

 


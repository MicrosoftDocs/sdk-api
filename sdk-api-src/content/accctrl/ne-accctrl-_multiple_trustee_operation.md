---
UID: NE:accctrl._MULTIPLE_TRUSTEE_OPERATION
title: "_MULTIPLE_TRUSTEE_OPERATION"
author: windows-sdk-content
description: Contains values that indicate whether a TRUSTEE structure is an impersonation trustee.
old-location: security\multiple_trustee_operation.htm
old-project: secauthz
ms.assetid: 00b00678-5c87-4aa9-8232-5f0f1cb48e24
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MULTIPLE_TRUSTEE_OPERATION, MULTIPLE_TRUSTEE_OPERATION enumeration [Security], NO_MULTIPLE_TRUSTEE, TRUSTEE_IS_IMPERSONATE, _MULTIPLE_TRUSTEE_OPERATION, _win32_multiple_trustee_operation_str, accctrl/MULTIPLE_TRUSTEE_OPERATION, accctrl/NO_MULTIPLE_TRUSTEE, accctrl/TRUSTEE_IS_IMPERSONATE, security.multiple_trustee_operation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: accctrl.h
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
req.typenames: MULTIPLE_TRUSTEE_OPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - MULTIPLE_TRUSTEE_OPERATION
product: Windows
targetos: Windows
---

# _MULTIPLE_TRUSTEE_OPERATION enumeration


## -description


The <b>MULTIPLE_TRUSTEE_OPERATION</b> enumeration contains values that indicate whether a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure is an impersonation trustee.


## -enum-fields




### -field NO_MULTIPLE_TRUSTEE

The trustee is not an impersonation trustee.


### -field TRUSTEE_IS_IMPERSONATE

The trustee is an impersonation trustee. The <b>pMultipleTrustee</b> member of the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure points to a trustee for a server that can impersonate the client trustee.


## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 


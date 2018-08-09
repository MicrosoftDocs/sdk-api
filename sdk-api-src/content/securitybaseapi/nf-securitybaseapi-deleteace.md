---
UID: NF:securitybaseapi.DeleteAce
title: DeleteAce function
author: windows-sdk-content
description: Deletes an access control entry (ACE) from an access control list (ACL).
old-location: security\deleteace.htm
old-project: secauthz
ms.assetid: 02ce45ad-3d51-4548-848e-a62bf4bf72a8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeleteAce, DeleteAce function [Security], _win32_deleteace, security.deleteace, securitybaseapi/DeleteAce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DeleteAce
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# DeleteAce function


## -description


The <b>DeleteAce</b> function deletes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) from an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. The ACE specified by the <i>dwAceIndex</i> parameter is removed from this ACL.


### -param dwAceIndex [in]

The ACE to delete. A value of zero corresponds to the first ACE in the ACL, a value of one to the second ACE, and so on.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An application can use the 
<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a> structure retrieved by the 
<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a> function to discover the size of the ACL and the number of ACEs it contains. The 
<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a> function retrieves information about an individual ACE.




## -see-also




<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a>



<a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/34f22aea-9cde-411e-b2d5-bfcd3bfe325d">AddAuditAccessAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>
 

 


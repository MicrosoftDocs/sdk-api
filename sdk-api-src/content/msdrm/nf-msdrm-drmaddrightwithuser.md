---
UID: NF:msdrm.DRMAddRightWithUser
title: DRMAddRightWithUser function
author: windows-sdk-content
description: Assigns a right to a user in an issuance license.
old-location: rm\drmaddrightwithuser.htm
old-project: AdRms_Sdk
ms.assetid: 10b76b20-cee7-44f3-b9bd-2b690fdd040c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMAddRightWithUser, DRMAddRightWithUser function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAddRightWithUser, rm.drmaddrightwithuser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMAddRightWithUser
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMAddRightWithUser function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAddRightWithUser</b> function assigns a right to a user in an issuance license.


## -parameters




### -param hIssuanceLicense [in]

The handle of the issuance license to add the right to. This handle is obtained by using the <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> function.


### -param hRight [in]

The handle of the right to add to the issuance license. This handle is obtained by using the <a href="https://msdn.microsoft.com/05074fbd-9268-41b4-a916-a932dc7a7858">DRMCreateRight</a> function.


### -param hUser [in]

The handle of the user to apply the right to. This handle is obtained by using the <a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a> function.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Because there is no way to remove a particular user right   (to remove all user rights, use the <a href="https://msdn.microsoft.com/f0a5dc8d-2bc6-4fcc-8871-ea80fc6a4abc">DRMClearAllRights</a> function), we recommend that you collect all user and right information first, and then bind users to rights after all changes have been made.

All rights added must be specifically recognized and handled by the application. An application is not required to handle any standard XrML rights except EDIT. If a user is allowed to edit the content in any way (for example, a user is granted a custom "ADDCOMMENT" right), the user must also be granted the standard XrML EDIT right.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>



<a href="https://msdn.microsoft.com/05074fbd-9268-41b4-a916-a932dc7a7858">DRMCreateRight</a>



<a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a>
 

 


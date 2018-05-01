---
UID: NF:msdrm.DRMGetUserInfo
title: DRMGetUserInfo function
author: windows-driver-content
description: Obtains information about a user.
old-location: rm\drmgetuserinfo.htm
old-project: AdRms_Sdk
ms.assetid: 98c0640d-8ee1-4072-989d-16a2e8ba09b3
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: DRMGetUserInfo, DRMGetUserInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUserInfo, rm.drmgetuserinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	DRMGetUserInfo
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetUserInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUserInfo</b> function obtains information about a user.


## -parameters




### -param hUser [in]

The handle of the user to obtain information for.


### -param puUserNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszUserName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszUserName</i> buffer.


### -param wszUserName [out]

A pointer to a null-terminated Unicode string that receives the user name as a fully qualified SMTP email address. This is not enforced or used to check identities; it is only included to provide a human-readable identification. The size of this buffer is specified by the <i>puUserNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puUserNameLength</i> value.


### -param puUserIdLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszUserId</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszUserId</i> buffer.


### -param wszUserId [out]

A pointer to a null-terminated Unicode string that receives the  user's ID. The size of this buffer is specified by the <i>puUserIdLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puUserIdLength</i> value.


### -param puUserIdTypeLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszUserIdType</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszUserIdType</i> buffer.


### -param wszUserIdType [out]

A pointer to a null-terminated Unicode string that receives the type of ID used to identify the user (such as Passport, Windows, or other). The size of this buffer is specified by the <i>puUserIdTypeLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puUserIdTypeLength</i> value.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



For more information about user IDs and ID types, see <a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a>.

When you obtain the output values, you can first call this function with <i>wszUserName</i>, <i>wszUserId</i>, and <i>wszUserIdType</i> set to <b>NULL</b> to obtain the needed buffer sizes through <i>puUserNameLength</i>, <i>puUserIdLength</i>, and <i>puUserIdTypeLength</i>. It is the application's responsibility to allocate and free buffer space.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a>



<a href="https://msdn.microsoft.com/4c8c8249-2e90-4eea-9a3b-dd7d9970ba98">DRMGetUsers</a>
 

 


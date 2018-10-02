---
UID: NS:msdrmdefs._DRMBOUNDLICENSEPARAMS
title: "_DRMBOUNDLICENSEPARAMS"
author: windows-sdk-content
description: Used by DRMCreateBoundLicense to bind to a license.
old-location: rm\drmboundlicenseparams.htm
tech.root: AdRms_Sdk
ms.assetid: 25820f49-ffa8-40c4-87fc-ce4909ec20ed
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMBINDINGFLAGS_IGNORE_VALIDITY_INTERVALS, DRMBOUNDLICENSEPARAMS, DRMBOUNDLICENSEPARAMS structure [Active Directory Rights Management Services SDK 1.0], _DRMBOUNDLICENSEPARAMS, msdrmdefs/DRMBOUNDLICENSEPARAMS, rm.drmboundlicenseparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msdrmdefs.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRMBOUNDLICENSEPARAMS
product: Windows
targetos: Windows
req.typenames: DRMBOUNDLICENSEPARAMS
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DRMBOUNDLICENSEPARAMS structure


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMBOUNDLICENSEPARAMS</b> structure is used by <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> to bind to a license.


## -struct-fields




### -field uVersion

Specifies the version of the structure. This member should be set to <b>DRMBOUNDLICENSEPARAMSVERSION</b>.


### -field hEnablingPrincipal

A handle to an enabling principal in the <a href="https://msdn.microsoft.com/en-us/library/Aa362618(v=VS.85).aspx">end-user license</a> that should be bound. Create this handle by using the <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a> function. The default for this member is <b>NULL</b>. If <b>NULL</b> is used, the application will bind to the first principal in the license.


### -field hSecureStore

Reserved for future use. This member must be set to <b>NULL</b>.


### -field wszRightsRequested

A pointer to a null-terminated Unicode string that contains a comma-delimited list of the rights requested. This member cannot be <b>NULL</b>, and the string must contain valid rights such as EDIT and OWNER.


### -field wszRightsGroup

A pointer to a null-terminated Unicode string that contains the name of the rights group to use in the license; for more information, see Remarks. This member can be set to <b>NULL</b> if it is not used.


### -field idResource

A <a href="https://msdn.microsoft.com/8b7f22e0-586e-4950-94fe-868b3fc91ffa">DRMID</a> structure that identifies the content to which you are trying to bind. You must set the <i>wszID</i> and <i>wszIDType</i> parameters of this structure to the  values you  specified in the <i>wszContentId</i> and <i>wszContentIdType</i> parameters, respectively, in the <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a> function. If the values are <b>NULL</b> or they do not match the corresponding values in <b>DRMSetMetaData</b>,  the <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> function returns an error.


### -field cAuthenticatorCount

Reserved for future use. This member must be set to zero.


### -field rghAuthenticators

Reserved for future use. This member must be set to <b>NULL</b>.


### -field wszDefaultEnablingPrincipalCredentials

A pointer to a null-terminated Unicode string that contains the certificate for the enabling principal (the <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a>). This member can be set to <b>NULL</b> if it is not used.


### -field dwFlags

Optional. Contains flags for additional settings. This member can be zero or the following value.



#### DRMBINDINGFLAGS_IGNORE_VALIDITY_INTERVALS

Normally, a bind will fail if the <a href="https://msdn.microsoft.com/en-us/library/Aa362618(v=VS.85).aspx">end-user license</a> has an expired certificate chain. However, if this flag is passed and the user's <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa362706(v=VS.85).aspx">machine certificate</a> are valid, and all other license requirements are valid, the bind will succeed. When this occurs, the application should alert the user that the content cannot be verified, and it will be opened at the user's risk.


## -remarks



In a C++ application, this structure has a default constructor that initializes the members to the following values.


```cpp
uVersion = DRMBOUNDLICENSEPARAMSVERSION
hEnablingPrincipal = NULL
hSecureStore = NULL
wszRightsRequested = NULL
wszRightsGroup = NULL
cAuthenticatorCount = 0
rghAuthenticators = NULL
wszDefaultEnablingPrincipalCredentials = NULL
idResource.uVersion = DRMIDVERSION
idResource.wszIDType = NULL
idResource.wszID = NULL
dwFlags = 0
```


If there is more than one rights group in the <a href="https://msdn.microsoft.com/en-us/library/Aa362618(v=VS.85).aspx">end-user license</a>, the <i>wszRightsGroup</i> parameter specifies the name of the rights group to use. By default, the first rights group found in the end-user license is chosen. If any one of the requested rights is not granted, the bind request (<a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>) will fail.




## -see-also




<a href="https://msdn.microsoft.com/06a0c6d2-108d-4c72-9ae6-8959304602c5">AD RMS Structures</a>



<a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>
 

 


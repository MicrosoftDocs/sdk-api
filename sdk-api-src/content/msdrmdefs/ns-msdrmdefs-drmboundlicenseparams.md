---
UID: NS:msdrmdefs._DRMBOUNDLICENSEPARAMS
title: DRMBOUNDLICENSEPARAMS (msdrmdefs.h)
description: Used by DRMCreateBoundLicense to bind to a license.
helpviewer_keywords: ["DRMBINDINGFLAGS_IGNORE_VALIDITY_INTERVALS","DRMBOUNDLICENSEPARAMS","DRMBOUNDLICENSEPARAMS structure [Active Directory Rights Management Services SDK 1.0]","msdrmdefs/DRMBOUNDLICENSEPARAMS","rm.drmboundlicenseparams"]
old-location: rm\drmboundlicenseparams.htm
tech.root: rm
ms.assetid: 25820f49-ffa8-40c4-87fc-ce4909ec20ed
ms.date: 12/05/2018
ms.keywords: DRMBINDINGFLAGS_IGNORE_VALIDITY_INTERVALS, DRMBOUNDLICENSEPARAMS, DRMBOUNDLICENSEPARAMS structure [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRMBOUNDLICENSEPARAMS, rm.drmboundlicenseparams
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
targetos: Windows
req.typenames: DRMBOUNDLICENSEPARAMS
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMBOUNDLICENSEPARAMS
 - msdrmdefs/_DRMBOUNDLICENSEPARAMS
 - DRMBOUNDLICENSEPARAMS
 - msdrmdefs/DRMBOUNDLICENSEPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRMBOUNDLICENSEPARAMS
---

# DRMBOUNDLICENSEPARAMS structure


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMBOUNDLICENSEPARAMS</b> structure is used by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> to bind to a license.

## -struct-fields

### -field uVersion

Specifies the version of the structure. This member should be set to <b>DRMBOUNDLICENSEPARAMSVERSION</b>.

### -field hEnablingPrincipal

A handle to an enabling principal in the <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a> that should be bound. Create this handle by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a> function. The default for this member is <b>NULL</b>. If <b>NULL</b> is used, the application will bind to the first principal in the license.

### -field hSecureStore

Reserved for future use. This member must be set to <b>NULL</b>.

### -field wszRightsRequested

A pointer to a null-terminated Unicode string that contains a comma-delimited list of the rights requested. This member cannot be <b>NULL</b>, and the string must contain valid rights such as EDIT and OWNER.

### -field wszRightsGroup

A pointer to a null-terminated Unicode string that contains the name of the rights group to use in the license; for more information, see Remarks. This member can be set to <b>NULL</b> if it is not used.

### -field idResource

A <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmid">DRMID</a> structure that identifies the content to which you are trying to bind. You must set the <i>wszID</i> and <i>wszIDType</i> parameters of this structure to the  values you  specified in the <i>wszContentId</i> and <i>wszContentIdType</i> parameters, respectively, in the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a> function. If the values are <b>NULL</b> or they do not match the corresponding values in <b>DRMSetMetaData</b>,  the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> function returns an error.

### -field cAuthenticatorCount

Reserved for future use. This member must be set to zero.

### -field rghAuthenticators

Reserved for future use. This member must be set to <b>NULL</b>.

### -field wszDefaultEnablingPrincipalCredentials

A pointer to a null-terminated Unicode string that contains the certificate for the enabling principal (the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a>). This member can be set to <b>NULL</b> if it is not used.

### -field dwFlags

Optional. Contains flags for additional settings. This member can be zero or the following value.



#### DRMBINDINGFLAGS_IGNORE_VALIDITY_INTERVALS

Normally, a bind will fail if the <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a> has an expired certificate chain. However, if this flag is passed and the user's <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> and <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificate</a> are valid, and all other license requirements are valid, the bind will succeed. When this occurs, the application should alert the user that the content cannot be verified, and it will be opened at the user's risk.

### -field _DRMBOUNDLICENSEPARAMS

TBD

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


If there is more than one rights group in the <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a>, the <i>wszRightsGroup</i> parameter specifies the name of the rights group to use. By default, the first rights group found in the end-user license is chosen. If any one of the requested rights is not granted, the bind request (<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>) will fail.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-structures">AD RMS Structures</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>
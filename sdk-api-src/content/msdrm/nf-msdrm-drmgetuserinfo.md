---
UID: NF:msdrm.DRMGetUserInfo
title: DRMGetUserInfo function (msdrm.h)
description: Obtains information about a user.
helpviewer_keywords: ["DRMGetUserInfo","DRMGetUserInfo function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUserInfo","rm.drmgetuserinfo"]
old-location: rm\drmgetuserinfo.htm
tech.root: rm
ms.assetid: 98c0640d-8ee1-4072-989d-16a2e8ba09b3
ms.date: 12/05/2018
ms.keywords: DRMGetUserInfo, DRMGetUserInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUserInfo, rm.drmgetuserinfo
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMGetUserInfo
 - msdrm/DRMGetUserInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetUserInfo
---

# DRMGetUserInfo function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

For more information about user IDs and ID types, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a>.

When you obtain the output values, you can first call this function with <i>wszUserName</i>, <i>wszUserId</i>, and <i>wszUserIdType</i> set to <b>NULL</b> to obtain the needed buffer sizes through <i>puUserNameLength</i>, <i>puUserIdLength</i>, and <i>puUserIdTypeLength</i>. It is the application's responsibility to allocate and free buffer space.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetusers">DRMGetUsers</a>
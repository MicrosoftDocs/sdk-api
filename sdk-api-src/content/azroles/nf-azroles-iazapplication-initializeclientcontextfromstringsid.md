---
UID: NF:azroles.IAzApplication.InitializeClientContextFromStringSid
title: IAzApplication::InitializeClientContextFromStringSid
author: windows-sdk-content
description: Gets an IAzClientContext object pointer from the specified security identifier (SID) in text form.
old-location: security\iazapplication_initializeclientcontextfromstringsid.htm
old-project: secauthz
ms.assetid: b718b0bf-bb11-4485-a4d8-0a90aab62165
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzApplication object [Security],InitializeClientContextFromStringSid method, IAzApplication interface [Security],InitializeClientContextFromStringSid method, IAzApplication.InitializeClientContextFromStringSid, IAzApplication::InitializeClientContextFromStringSid, InitializeClientContextFromStringSid, InitializeClientContextFromStringSid method [Security], InitializeClientContextFromStringSid method [Security],AzApplication object, InitializeClientContextFromStringSid method [Security],IAzApplication interface, azroles/IAzApplication::InitializeClientContextFromStringSid, security.iazapplication_initializeclientcontextfromstringsid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.InitializeClientContextFromStringSid
 - AzApplication.InitializeClientContextFromStringSid
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::InitializeClientContextFromStringSid


## -description


The <b>InitializeClientContextFromStringSid</b> method gets an <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object pointer from the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form.<div class="alert"><b>Note</b>  If possible, call the <a href="https://msdn.microsoft.com/0002804d-0e97-4648-8aa1-14eba09a90fa">InitializeClientContextFromToken</a>  function instead of <b>InitializeClientContextFromStringSid</b>. For more information, see Remarks.</div>
<div> </div>



## -parameters




### -param SidString [in]

A string that contains the text form of the SID of the security principal. This must be a valid string SID that can be converted by the <a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a> function.


### -param lOptions [in]

Options for the context creation.

If AZ_CLIENT_CONTEXT_SKIP_GROUP is specified, the SID specified in the <i>SidString</i> parameter is not necessarily a valid user account. The SID will be used to create the context without validation. The created context will be flagged as having been created from a SID,  the  SID string will be stored in the client name field, and the domain name field will be empty. Token groups will not be used in the client context creation. <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Lightweight Directory Access Protocol</a> (LDAP) query groups are not supported when AZ_CLIENT_CONTEXT_SKIP_GROUP is specified. Because the account is not validated in Active Directory, the client context's user information properties, such as <a href="https://msdn.microsoft.com/3b1f9e8a-cc3b-4be6-b2d9-8e8b3164d46a">UserSamCompat</a>, will not be valid, and when accessed, they  will return ERROR_INVALID_HANDLE. The <a href="https://msdn.microsoft.com/817b3693-b989-431c-a8b3-bdeeb0367dc6">RoleForAccessCheck</a> property and the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method of <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> can still be used to specify a role for access checking. The <a href="https://msdn.microsoft.com/753506cc-ed44-4795-90e5-c76010181d8a">GetRoles</a> method of <b>IAzClientContext</b> can still be used to enumerate  roles assigned to the context within a specific scope.

If AZ_CLIENT_CONTEXT_SKIP_GROUP is not specified, the SID must represent a valid  user account.


### -param varReserved [in, optional]

Reserved for future use. This parameter can be one of the following values:

<ul>
<li>varReserved.vt == VT_ERROR and varReserved.scode == DISP_E_PARAMNOTFOUND</li>
<li>varReserved.vt == VT_EMPTY</li>
<li>varReserved.vt == VT_NULL</li>
<li>varReserved.vt == VT_I4 and varReserved.lVal == 0</li>
<li>varReserved.vt == VT_I2 and varReserved.iVal == 0</li>
</ul>

### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If possible, call the <a href="https://msdn.microsoft.com/0002804d-0e97-4648-8aa1-14eba09a90fa">InitializeClientContextFromToken</a>  function instead of <b>InitializeClientContextFromStringSid</b>. <b>InitializeClientContextFromStringSid</b> attempts to retrieve the information available in a logon token had the client actually logged on. An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon. The client context  created by <b>InitializeClientContextFromToken</b> uses a logon token, and the resulting client context is more complete and accurate than a client context created by <b>InitializeClientContextFromStringSid</b>.

<div class="alert"><b>Important</b>  Applications should not assume that the calling context has permission to use this function. The <a href="https://msdn.microsoft.com/402a8641-5644-45c1-80e9-c60321c1ac38">AuthzInitializeContextFromSid</a> function reads the tokenGroupsGlobalAndUniversal attribute of the SID specified in the call to determine the current user's group memberships. If the user's object is in <a href="https://msdn.microsoft.com/9fc78c72-c59c-4c4d-ace5-00a431645c4b">Active Directory</a>, the calling context must have read access to the tokenGroupsGlobalAndUniversal attribute on the user object. Read access to the tokenGroupsGlobalAndUniversal attribute is granted  to the <b>Pre-Windows 2000 Compatible Access</b> group, but new domains contain an empty <b>Pre-Windows 2000 Compatible Access</b> group by default because the default setup selection is <b>Permissions compatible with Windows 2000 and Windows Server 2003</b>. Therefore, applications may not have access to the tokenGroupsGlobalAndUniversal attribute; in this case, the <b>AuthzInitializeContextFromSid</b> function  fails with ACCESS_DENIED. Applications that use this function should correctly handle this error and provide supporting documentation. To simplify granting accounts permission to query a user's group information, add accounts that need the ability to look up group information to the Windows Authorization Access Group.</div>
<div> </div>
Applications calling this function should use the fully qualified domain name or <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN). Otherwise, this method might fail across forests if the NetBIOS domain name is used and the two domains do not have a direct trust relationship.




## -see-also




<a href="https://msdn.microsoft.com/3d813e46-f06e-4147-874c-30b5fc6f50d9">Allowing Anonymous Access</a>



<a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>
 

 


---
UID: NF:azroles.IAzApplication.InitializeClientContextFromName
title: IAzApplication::InitializeClientContextFromName (azroles.h)
description: Gets an IAzClientContext object pointer from the client identity as a (domain name, client name) pair.
helpviewer_keywords: ["AzApplication object [Security]","InitializeClientContextFromName method","IAzApplication interface [Security]","InitializeClientContextFromName method","IAzApplication.InitializeClientContextFromName","IAzApplication::InitializeClientContextFromName","InitializeClientContextFromName","InitializeClientContextFromName method [Security]","InitializeClientContextFromName method [Security]","AzApplication object","InitializeClientContextFromName method [Security]","IAzApplication interface","azroles/IAzApplication::InitializeClientContextFromName","security.iazapplication_initializeclientcontextfromname"]
old-location: security\iazapplication_initializeclientcontextfromname.htm
tech.root: security
ms.assetid: 25628f06-fea7-4acd-b1db-b3667fcd07a2
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],InitializeClientContextFromName method, IAzApplication interface [Security],InitializeClientContextFromName method, IAzApplication.InitializeClientContextFromName, IAzApplication::InitializeClientContextFromName, InitializeClientContextFromName, InitializeClientContextFromName method [Security], InitializeClientContextFromName method [Security],AzApplication object, InitializeClientContextFromName method [Security],IAzApplication interface, azroles/IAzApplication::InitializeClientContextFromName, security.iazapplication_initializeclientcontextfromname
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::InitializeClientContextFromName
 - azroles/IAzApplication::InitializeClientContextFromName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.InitializeClientContextFromName
 - AzApplication.InitializeClientContextFromName
---

# IAzApplication::InitializeClientContextFromName


## -description

The <b>InitializeClientContextFromName</b> method gets an <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object pointer from the client identity as a (domain name, client name) pair. <div class="alert"><b>Note</b>  If possible, call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken">InitializeClientContextFromToken</a>  function instead of <b>InitializeClientContextFromName</b>. For more information, see Remarks.</div>
<div> </div>

## -parameters

### -param ClientName [in]

Name of the security principal.

### -param DomainName [in, optional]

Domain name in which the user account resides. The default value is <b>NULL</b>.

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

A pointer to a pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If possible, call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken">InitializeClientContextFromToken</a>  function instead of <b>InitializeClientContextFromName</b>. <b>InitializeClientContextFromName</b> attempts to retrieve the information available in a logon token had the client actually logged on. An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon. The client context  created by <b>InitializeClientContextFromToken</b> uses a logon token, and the resulting client context is more complete and accurate than a client context created by <b>InitializeClientContextFromName</b>.

The <i>DomainName</i> and <i>ClientName</i> parameters must combine to represent a <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SidTypeUser</a>.

The supported name formats are the same as those supported by the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function.

<div class="alert"><b>Important</b>  Applications should not assume that the calling context has permission to use this function. The <a href="/windows/desktop/api/authz/nf-authz-authzinitializecontextfromsid">AuthzInitializeContextFromSid</a> function reads the tokenGroupsGlobalAndUniversal attribute of the SID specified in the call to determine the current user's group memberships. If the user's object is in <a href="/windows/desktop/AD/active-directory-domain-services">Active Directory</a>, the calling context must have read access to the tokenGroupsGlobalAndUniversal attribute on the user object. Read access to the tokenGroupsGlobalAndUniversal attribute is granted  to the <b>Pre-Windows 2000 Compatible Access</b> group, but new domains contain an empty <b>Pre-Windows 2000 Compatible Access</b> group by default because the default setup selection is <b>Permissions compatible with Windows 2000 and Windows Server 2003</b>. Therefore, applications may not have access to the tokenGroupsGlobalAndUniversal attribute; in this case, the <b>AuthzInitializeContextFromSid</b> function  fails with ACCESS_DENIED. Applications that use this function should correctly handle this error and provide supporting documentation. To simplify granting accounts permission to query a user's group information, add accounts that need the ability to look up group information to the Windows Authorization Access Group.</div>
<div> </div>
Applications calling this function should use the fully qualified domain name or <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN). Otherwise, this method might fail across forests if the NetBIOS domain name is used and the two domains do not have a direct trust relationship.

## -see-also

<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Allowing Anonymous Access</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a>
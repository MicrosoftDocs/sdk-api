---
UID: NF:msdrm.DRMCreateUser
title: DRMCreateUser function (msdrm.h)
description: Creates a user that will be granted a right.
helpviewer_keywords: ["DRMCreateUser","DRMCreateUser function [Active Directory Rights Management Services SDK 1.0]","Federation","Internal","Passport","Unspecified","Windows","msdrm/DRMCreateUser","rm.drmcreateuser"]
old-location: rm\drmcreateuser.htm
tech.root: rm
ms.assetid: e5679f4f-23e7-40af-9f45-d2077643da98
ms.date: 12/05/2018
ms.keywords: DRMCreateUser, DRMCreateUser function [Active Directory Rights Management Services SDK 1.0], Federation, Internal, Passport, Unspecified, Windows, msdrm/DRMCreateUser, rm.drmcreateuser
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
 - DRMCreateUser
 - msdrm/DRMCreateUser
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
 - DRMCreateUser
---

# DRMCreateUser function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateUser</b> function creates a user that 
    will be granted a right.

## -parameters

### -param wszUserName [in]

A null-terminated string that identifies a user or group of users (see Remarks). This parameter is often an 
       email address.  When the user created is passed in as <i>hOwner</i> to 
       <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>, this value is 
       attached to the Owner node in the license XrML. For more information about possible values for this parameter, 
       see the <i>wszUserIdType</i> parameter.

### -param wszUserId [in]

A null-terminated string that identifies a user that will be granted a right. This parameter can be a 
       Passport ID (PUID), Windows ID <a href="/previous-versions/windows/desktop/adrms_sdk/s-gly">security ID</a> (SID), or 
       <b>NULL</b>. If this parameter is <b>NULL</b>, 
       <i>wszUserIdType</i> must contain "Unspecified". This ID is verified by the 
       Active Directory Rights Management Services system. For more information about possible values for this 
       parameter, see the <i>wszUserIdType</i> parameter.

### -param wszUserIdType [in]

The user ID type. This parameter can be one of the following values.



#### "Windows"

For this value, <i>wszUserName</i> and <i>wszUserId</i> can contain 
         the following.





##### wszUserName

Fully qualified SMTP address. Can be <b>NULL</b> if 
            <i>wszUserId</i> contains a SID.



##### wszUserId

Optional SID (used for decorative purposes only; not verified). If not given, the license records 
            "Unspecified".



#### "Passport"

For this value, <i>wszUserName</i> and <i>wszUserId</i> can contain 
         the following.





##### wszUserName

Fully qualified SMTP address. Required in all cases.



##### wszUserId

Optional PUID (used for decorative purposes only; not verified). If not given, the license records 
            "Unspecified".



#### "Unspecified"

For this value, <i>wszUserName</i> and <i>wszUserId</i> can contain 
         the following.





##### wszUserName

Fully qualified SMTP address. Required in all cases.



##### wszUserId

<b>NULL</b> (see Remarks).



#### "Internal"

For this value, <i>wszUserName</i> and <i>wszUserId</i> can contain 
         the following.





##### wszUserName

<b>NULL</b>



##### wszUserId

One of the following:





###### "Anyone"

A license will be granted to anyone who requests one, but it will be attached to the requesting 
               user.



###### "Owner"

A license will be granted to the owner, specified in 
               <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>.



#### "Federation"

For this value, <i>wszUserName</i> and <i>wszUserId</i> can contain 
         the following.





##### wszUserName

Fully qualified SMTP address. Can be <b>NULL</b> if <i>wszUserId
            </i> contains a SID.



##### wszUserId

Optional SID (used for decorative purposes only; not verified). If not given, the license records 
            "Unspecified".

### -param phUser [out]

A pointer to the handle of the created user. Call 
       <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For 
       a list of common error codes, see 
       <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

At license request time, a user must present a rights account certificate identifying themselves by SID or PUID 
     if the user ID is WINDOWS or PASSPORT. If the user ID type is UNSPECIFIED (that is, if you do not know if it will 
     be Windows, Passport, or some other type), you can simply enter an email address of a client, and the AD RMS 
     system will use the email address alone to verify identity. However, this method is much less secure.

Windows authorization is used when a client is within an enterprise with its own license server (typically this 
     occurs over a LAN or Virtual Private Network). When a client will be requesting a use license from a server 
     outside an enterprise (typically over the Internet), you should use Passport authorization. To use Passport 
     authorization on your AD RMS service, go to the AD RMS Global Administration webpage, view the 
     <b>Trust Policies</b> page, and then click <b>Trust Passport RACs</b>. 
     You may mix Windows and Passport users in a single issuance license.

If you want to create an issuance license for a group of people under an email distribution list (such as 
     marketing@contoso.com), insert the fully qualified distribution list name into 
     <i>wszUserName</i>, and leave <i>wszUserId</i> empty. The server will 
     expand the distribution list when obtaining the use license. Note that this can cause a performance lag if the 
     distribution list contains several nested distribution lists within it.

Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle of the 
     user object  created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/onlinesigning-getunsignedil-cpp">OnlineSigning_GetUnsignedIL.cpp</a>
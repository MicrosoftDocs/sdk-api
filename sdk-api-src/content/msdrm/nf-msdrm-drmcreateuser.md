---
UID: NF:msdrm.DRMCreateUser
title: DRMCreateUser function
author: windows-sdk-content
description: Creates a user that will be granted a right.
old-location: rm\drmcreateuser.htm
old-project: AdRms_Sdk
ms.assetid: e5679f4f-23e7-40af-9f45-d2077643da98
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMCreateUser, DRMCreateUser function [Active Directory Rights Management Services SDK 1.0], Federation, Internal, Passport, Unspecified, Windows, msdrm/DRMCreateUser, rm.drmcreateuser
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMCreateUser
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateUser function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateUser</b> function creates a user that 
    will be granted a right.


## -parameters




### -param wszUserName [in]

A null-terminated string that identifies a user or group of users (see Remarks). This parameter is often an 
       email address.  When the user created is passed in as <i>hOwner</i> to 
       <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>, this value is 
       attached to the Owner node in the license XrML. For more information about possible values for this parameter, 
       see the <i>wszUserIdType</i> parameter.


### -param wszUserId [in]

A null-terminated string that identifies a user that will be granted a right. This parameter can be a 
       Passport ID (PUID), Windows ID <a href="https://msdn.microsoft.com/library/ms682866(v=VS.85).aspx">security ID</a> (SID), or 
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
               <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>.



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
       <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For 
       a list of common error codes, see 
       <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




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

Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle of the 
     user object  created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/19387d86-6dbc-436f-8772-b9f25458460e">OnlineSigning_GetUnsignedIL.cpp</a>
 

 


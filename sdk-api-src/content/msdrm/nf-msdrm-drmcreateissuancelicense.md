---
UID: NF:msdrm.DRMCreateIssuanceLicense
title: DRMCreateIssuanceLicense function
author: windows-sdk-content
description: Creates an issuance license from scratch, from a template, or from a signed issuance license.
old-location: rm\drmcreateissuancelicense.htm
tech.root: AdRms_Sdk
ms.assetid: db2e9aa6-7021-4805-8fd7-94c8d02776b0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DRMCreateIssuanceLicense, DRMCreateIssuanceLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateIssuanceLicense, rm.drmcreateissuancelicense
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMCreateIssuanceLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateIssuanceLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available 
    for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, 
    Windows 7, Windows Server 2012, and Windows 8. It may be altered or 
    unavailable in subsequent versions. Instead, use 
    <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 
    which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateIssuanceLicense</b> function 
    creates an <a href="i_gly.htm">issuance license</a> from scratch, from a template, or from a signed issuance license.


## -parameters




### -param pstTimeFrom [in]

The starting UTC validity time for the license. If this value is <b>NULL</b>, the <i>pstTimeUntil</i> parameter must also be <b>NULL</b>. If both parameters are not <b>NULL</b>, <b>E_DRM_INVALID_TIMEINFO</b> is returned if the range time is logically inconsistent. For example, <i>pstTimeFrom</i> cannot be later than <i>pstTimeUntil</i>.


### -param pstTimeUntil [in]

The ending UTC validity time for the license. If this value is <b>NULL</b>, the <i>pstTimeFrom</i> parameter must also be <b>NULL</b>. If both parameters are not <b>NULL</b>, <b>E_DRM_INVALID_TIMEINFO</b> is returned if the range time is logically inconsistent. For example, <i>pstTimeFrom</i> cannot be later than <i>pstTimeUntil</i>.


### -param wszReferralInfoName [in]

Nonsilent license acquisition is not supported; set this parameter to <b>NULL</b>.

For Rights Management Services (RMS) client 1.0, this parameter is a pointer to a null-terminated Unicode string that contains the display name for the URL in <i>wszReferralInfoURL</i>. This parameter is optional and can be <b>NULL</b>.


### -param wszReferralInfoURL [in]

Nonsilent license acquisition is not supported; set this parameter to <b>NULL</b>.

For RMS client 1.0, this parameter is a pointer to a null-terminated Unicode string that contains the URL where an application should go to request a license for the content nonsilently. This should be an HTML page that hosts the ActiveX control. This parameter is optional and can be <b>NULL</b>.


### -param hOwner [in, optional]

A handle to the user that owns the issuance license. The handle is created by calling  the <a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a> function. The owner is identified under the <b>Owner</b> node in the issuance license XrML. This parameter is optional and can be <b>NULL</b>.

Do not confuse the owner of an issuance license with a user who has been granted the OWNER right. Ownership of an issuance license does not automatically grant any rights to use or modify content.  Specifying a value for the optional <i>hOwner</i> parameter merely enables an application to identify the content owner or author. The ID is added as metadata to the license. The OWNER right, on the other hand, grants a user the authority to exercise all rights contained in the license. Granting yourself (or anyone else) the OWNER right must be done explicitly by using <a href="https://msdn.microsoft.com/10b76b20-cee7-44f3-b9bd-2b690fdd040c">DRMAddRightWithUser</a>. Zero, one, or more users can be granted the OWNER right, which never expires.

If specified, the issuance license owner is added as metadata beneath the &lt;WORK&gt; node of the license.


```
<WORK>
  <OBJECT type="contentType">
    <ID type="contentIdType">contentId</ID>
    <NAME>contentName</NAME>
  </OBJECT>
  <METADATA>
    <OWNER>
      <OBJECT>
        <ID type="Windows"/>
        <NAME>david@contoso.com</NAME>
      </OBJECT>
    </OWNER>
  </METADATA>
  ...

```


If granted, the OWNER right is added as an attribute of the &lt;RIGHT&gt; element in the license XrML.


```
<WORK>
  ...
  <RIGHTSGROUP name="MainRights">
    <RIGHTSLIST>
      <VIEW>
        ...
      </VIEW>
      <RIGHT name="OWNER">
        <CONDITIONLIST>
          ...
        </CONDITIONLIST>
      </RIGHT>
    </RIGHTSLIST>
  </RIGHTSGROUP>
```


<div class="alert"><b>Note</b>  In the case where you set <i>hOwner</i> to the license author and use a template where you check the <b>Grant Owner (author) full control right with no expiration</b> check box, the license author can subsequently get an end-user license with Owner rights. See <a href="https://msdn.microsoft.com/40e87b21-162c-408d-81ca-16443352ce16">Understanding XrML Rights</a> for more information.</div>
<div> </div>

### -param wszIssuanceLicense [in]

A pointer to a null-terminated Unicode string that contains an issuance license template or a signed issuance license. You can call the <a href="https://msdn.microsoft.com/6667bab3-5022-4279-846a-61a0a37e9d33">DRMGetIssuanceLicenseTemplate</a> function to retrieve  a template. If this parameter is <b>NULL</b>,  an issuance license is created.


### -param hBoundLicense [in]

A handle to a bound license that contains the VIEWRIGHTSDATA, EDITRIGHTSDATA or OWNER right, which allows an application to reuse rights data or reuse the content key from a previous issuance license. This parameter is optional and can be <b>NULL</b>. For further information about rights, see <a href="https://msdn.microsoft.com/40e87b21-162c-408d-81ca-16443352ce16">Understanding XrML Rights</a>.

<div class="alert"><b>Note</b>  If your intent is to create a new issuance license, but you want to use the content key from the original signed issuance license, ensure that the <i>hBoundLicense</i> you pass in to <b>DRMCreateIssuanceLicense</b> is bound to either the OWNER or EDITRIGHTSDATA right. In a subsequent call to <a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a>,  pass in the issuance license handle obtained from <b>DRMCreateIssuanceLicense</b> and  the DRM_REUSE_KEY flag in order to reuse the content key.</div>
<div> </div>

### -param phIssuanceLicense [out]

A pointer to a <a href="https://msdn.microsoft.com/485a747c-a5bc-4ed0-a8f8-da64e011316f">DRMPUBHANDLE</a> that receives the handle to the new issuance license.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



An issuance license is a list of rights, users, metadata, and other information that specifies how a specific user on a specific computer is able to use the specified content. This issuance license must be signed by using the <a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a> function or the <a href="https://msdn.microsoft.com/1dc1dc7f-4e63-4cc6-aa34-a8e44ce79655">AcquireIssuanceLicense</a> SOAP method. The resulting signed issuance license is given to a potential end user who must then request an <a href="e_gly.htm">end-user license</a> by calling the <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a> function. An application may request an end-user license on behalf of another end user by using the <a href="https://msdn.microsoft.com/fa21a8fd-6c35-4ef9-bf94-b1229b3a8b60">AcquirePreLicense</a> SOAP method. It is only the end-user license that allows an application to exercise the rights that have been granted.

This function allows you to create licenses in three different ways.

<table>
<tr>
<th><i>wszIssuanceLicense</i> value</th>
<th><i>hBoundLicense</i> value</th>
<th>Description</th>
</tr>
<tr>
<td>An unsigned issuance license from a file or an issuance license handle passed into <a href="https://msdn.microsoft.com/6667bab3-5022-4279-846a-61a0a37e9d33">DRMGetIssuanceLicenseTemplate</a>
</td>
<td><b>NULL</b></td>
<td>Use to create an issuance license from a template. The new issuance license contains information from the old issuance license (the list follows this table), but it does not reuse the content key. </td>
</tr>
<tr>
<td>A signed issuance license</td>
<td>A handle to the license bound by the OWNER or VIEWRIGHTSDATA right</td>
<td>Use to reuse rights information (the list follows this table).</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
<td>Use to create an issuance license from scratch. It includes no users, rights, metadata, or policies.</td>
</tr>
</table>
 


When an issuance license (signed or unsigned) is passed in, the following data is reused:

<ul>
<li>Users (from <a href="https://msdn.microsoft.com/e5679f4f-23e7-40af-9f45-d2077643da98">DRMCreateUser</a>)</li>
<li>Rights (from <a href="https://msdn.microsoft.com/05074fbd-9268-41b4-a916-a932dc7a7858">DRMCreateRight</a>)</li>
<li>Application-specific data (from <a href="https://msdn.microsoft.com/659b2d73-1160-4e5a-8779-4bb272653c54">DRMSetApplicationSpecificData</a>)</li>
<li>Metadata (from <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a>)</li>
<li>Name and description (from <a href="https://msdn.microsoft.com/c5dc8aa8-f45b-4b8a-bd83-0661db424303">DRMSetNameAndDescription</a>)</li>
<li>Revocation point (from <a href="https://msdn.microsoft.com/a9f4ff8d-1b9f-46f4-8a69-5957d4b2aefb">DRMSetRevocationPoint</a>)</li>
<li>Usage policy (from <a href="https://msdn.microsoft.com/8c270824-ff2a-4b04-b8b0-7cc4a82d042d">DRMSetUsagePolicy</a>)</li>
</ul>


Because nonsilent license acquisition is not supported, <i>wszReferralInfoName</i> and <i>wszReferralInfoURL</i> should be <b>NULL</b>.

For RMS client 1.0, the referral point described by <i>wszReferralInfoName</i> and <i>wszReferralInfoURL</i> is used as a backup URL if a call to the URL specified in the license header fails. This method allows a caller to define a display name and a URL to a site that handles nonsilent license requests for the content.

The <i>hBoundLicense</i> parameter allows an application to be able to reuse data from an existing issuance license. This is done by having the publishing application create a VIEWRIGHTSDATA right and grant it to any application allowed to reuse the issuance license information. However, because this involves binding to a license, which is a task that cannot be done without using a <a href="l_gly.htm">lockbox</a>, this value should be <b>NULL</b> for server applications that do not use a lockbox.

The purpose of a URL cannot be verified by any part of a client or Active Directory Rights Management Services system. It would be possible for a malicious publisher to include a harmful URL address in an issuance license, although the issuance license creator would need a valid licensed Active Directory Rights Management Services system to do so.

One problem that can arise when creating issuance licenses with short validity times is the problem of clock skew. Clock skew is when the publishing computer's clock and the end user's computer clock are not exactly aligned. Clock skew can cause issuance license signing attempts to fail. For more information, see <a href="https://msdn.microsoft.com/a265b2e8-b8ea-41d3-ae51-ca6019d68221">Clock Skew</a>.

Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the issuance license handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>
 

 


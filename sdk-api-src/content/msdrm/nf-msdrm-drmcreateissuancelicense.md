---
UID: NF:msdrm.DRMCreateIssuanceLicense
title: DRMCreateIssuanceLicense function (msdrm.h)
description: Creates an issuance license from scratch, from a template, or from a signed issuance license.
helpviewer_keywords: ["DRMCreateIssuanceLicense","DRMCreateIssuanceLicense function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateIssuanceLicense","rm.drmcreateissuancelicense"]
old-location: rm\drmcreateissuancelicense.htm
tech.root: rm
ms.assetid: db2e9aa6-7021-4805-8fd7-94c8d02776b0
ms.date: 12/05/2018
ms.keywords: DRMCreateIssuanceLicense, DRMCreateIssuanceLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateIssuanceLicense, rm.drmcreateissuancelicense
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
 - DRMCreateIssuanceLicense
 - msdrm/DRMCreateIssuanceLicense
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
 - DRMCreateIssuanceLicense
---

# DRMCreateIssuanceLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available 
    for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, 
    Windows 7, Windows Server 2012, and Windows 8. It may be altered or 
    unavailable in subsequent versions. Instead, use 
    <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 
    which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateIssuanceLicense</b> function 
    creates an <a href="/previous-versions/windows/desktop/adrms_sdk/i-gly">issuance license</a> from scratch, from a template, or from a signed issuance license.

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

A handle to the user that owns the issuance license. The handle is created by calling  the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a> function. The owner is identified under the <b>Owner</b> node in the issuance license XrML. This parameter is optional and can be <b>NULL</b>.

Do not confuse the owner of an issuance license with a user who has been granted the OWNER right. Ownership of an issuance license does not automatically grant any rights to use or modify content.  Specifying a value for the optional <i>hOwner</i> parameter merely enables an application to identify the content owner or author. The ID is added as metadata to the license. The OWNER right, on the other hand, grants a user the authority to exercise all rights contained in the license. Granting yourself (or anyone else) the OWNER right must be done explicitly by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a>. Zero, one, or more users can be granted the OWNER right, which never expires.

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


<div class="alert"><b>Note</b>  In the case where you set <i>hOwner</i> to the license author and use a template where you check the <b>Grant Owner (author) full control right with no expiration</b> check box, the license author can subsequently get an end-user license with Owner rights. See <a href="/previous-versions/windows/desktop/adrms_sdk/understanding-xrml-rights">Understanding XrML Rights</a> for more information.</div>
<div> </div>

### -param wszIssuanceLicense [in]

A pointer to a null-terminated Unicode string that contains an issuance license template or a signed issuance license. You can call the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicensetemplate">DRMGetIssuanceLicenseTemplate</a> function to retrieve  a template. If this parameter is <b>NULL</b>,  an issuance license is created.

### -param hBoundLicense [in]

A handle to a bound license that contains the VIEWRIGHTSDATA, EDITRIGHTSDATA or OWNER right, which allows an application to reuse rights data or reuse the content key from a previous issuance license. This parameter is optional and can be <b>NULL</b>. For further information about rights, see <a href="/previous-versions/windows/desktop/adrms_sdk/understanding-xrml-rights">Understanding XrML Rights</a>.

<div class="alert"><b>Note</b>  If your intent is to create a new issuance license, but you want to use the content key from the original signed issuance license, ensure that the <i>hBoundLicense</i> you pass in to <b>DRMCreateIssuanceLicense</b> is bound to either the OWNER or EDITRIGHTSDATA right. In a subsequent call to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a>,  pass in the issuance license handle obtained from <b>DRMCreateIssuanceLicense</b> and  the DRM_REUSE_KEY flag in order to reuse the content key.</div>
<div> </div>

### -param phIssuanceLicense [out]

A pointer to a <a href="/previous-versions/windows/desktop/adrms_sdk/drmpubhandle">DRMPUBHANDLE</a> that receives the handle to the new issuance license.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

An issuance license is a list of rights, users, metadata, and other information that specifies how a specific user on a specific computer is able to use the specified content. This issuance license must be signed by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a> function or the <a href="/previous-versions/windows/desktop/adrms_sdk/-acquireissuancelicense">AcquireIssuanceLicense</a> SOAP method. The resulting signed issuance license is given to a potential end user who must then request an <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a> by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a> function. An application may request an end-user license on behalf of another end user by using the <a href="/previous-versions/windows/desktop/adrms_sdk/-acquireprelicense">AcquirePreLicense</a> SOAP method. It is only the end-user license that allows an application to exercise the rights that have been granted.

This function allows you to create licenses in three different ways.

<table>
<tr>
<th><i>wszIssuanceLicense</i> value</th>
<th><i>hBoundLicense</i> value</th>
<th>Description</th>
</tr>
<tr>
<td>An unsigned issuance license from a file or an issuance license handle passed into <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicensetemplate">DRMGetIssuanceLicenseTemplate</a>
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
<li>Users (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a>)</li>
<li>Rights (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a>)</li>
<li>Application-specific data (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetapplicationspecificdata">DRMSetApplicationSpecificData</a>)</li>
<li>Metadata (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a>)</li>
<li>Name and description (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetnameanddescription">DRMSetNameAndDescription</a>)</li>
<li>Revocation point (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetrevocationpoint">DRMSetRevocationPoint</a>)</li>
<li>Usage policy (from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetusagepolicy">DRMSetUsagePolicy</a>)</li>
</ul>


Because nonsilent license acquisition is not supported, <i>wszReferralInfoName</i> and <i>wszReferralInfoURL</i> should be <b>NULL</b>.

For RMS client 1.0, the referral point described by <i>wszReferralInfoName</i> and <i>wszReferralInfoURL</i> is used as a backup URL if a call to the URL specified in the license header fails. This method allows a caller to define a display name and a URL to a site that handles nonsilent license requests for the content.

The <i>hBoundLicense</i> parameter allows an application to be able to reuse data from an existing issuance license. This is done by having the publishing application create a VIEWRIGHTSDATA right and grant it to any application allowed to reuse the issuance license information. However, because this involves binding to a license, which is a task that cannot be done without using a <a href="/previous-versions/windows/desktop/adrms_sdk/l-gly">lockbox</a>, this value should be <b>NULL</b> for server applications that do not use a lockbox.

The purpose of a URL cannot be verified by any part of a client or Active Directory Rights Management Services system. It would be possible for a malicious publisher to include a harmful URL address in an issuance license, although the issuance license creator would need a valid licensed Active Directory Rights Management Services system to do so.

One problem that can arise when creating issuance licenses with short validity times is the problem of clock skew. Clock skew is when the publishing computer's clock and the end user's computer clock are not exactly aligned. Clock skew can cause issuance license signing attempts to fail. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/clock-skew">Clock Skew</a>.

Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the issuance license handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>
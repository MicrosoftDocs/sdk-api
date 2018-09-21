---
UID: NF:certcli.ICertConfig.GetField
title: ICertConfig::GetField
author: windows-sdk-content
description: Gets a specific field from the current record of the configuration database. This method was first defined in the ICertConfig interface.
old-location: security\icertconfig2_getfield.htm
tech.root: seccrypto
ms.assetid: 8e477fa7-d0e7-43f3-98b5-79c924a1a29c
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: Authority, CCertConfig object [Security],GetField method, CommonName, Config, Country, Description, ExchangeCertificate, Flags, GetField, GetField method [Security], GetField method [Security],CCertConfig object, GetField method [Security],ICertConfig interface, GetField method [Security],ICertConfig2 interface, ICertConfig interface [Security],GetField method, ICertConfig.GetField, ICertConfig2 interface [Security],GetField method, ICertConfig2::GetField, ICertConfig::GetField, Locality, OrgUnit, Organization, SanitizedName, SanitizedShortName, Server, ShortName, SignatureCertificate, State, WebEnrollmentServers, _certsrv_icertconfig_getfield, certcli/ICertConfig2::GetField, certcli/ICertConfig::GetField, security.icertconfig2_getfield
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig2.GetField
 - ICertConfig.GetField
 - CCertConfig.GetField
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertConfig::GetField


## -description


The <b>GetField</b> method gets a specific field from the current record of the configuration database. This method was first defined in the <a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a> interface.


## -parameters




### -param strFieldName [in]

Specifies the name of the field to return. This parameter can be one of the following valid strings for field names (note that some certification authorities may not provide data for each field).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Authority"></a><a id="authority"></a><a id="AUTHORITY"></a><dl>
<dt><b>Authority</b></dt>
</dl>
</td>
<td width="60%">
Reference certification authority (CA) name.

</td>
</tr>
<tr>
<td width="40%"><a id="CommonName"></a><a id="commonname"></a><a id="COMMONNAME"></a><dl>
<dt><b>CommonName</b></dt>
</dl>
</td>
<td width="60%">
Common name of the server.

</td>
</tr>
<tr>
<td width="40%"><a id="Config"></a><a id="config"></a><a id="CONFIG"></a><dl>
<dt><b>Config</b></dt>
</dl>
</td>
<td width="60%">
Reference computer\CA name.

</td>
</tr>
<tr>
<td width="40%"><a id="Country"></a><a id="country"></a><a id="COUNTRY"></a><dl>
<dt><b>Country</b></dt>
</dl>
</td>
<td width="60%">
Country/region.

</td>
</tr>
<tr>
<td width="40%"><a id="Description"></a><a id="description"></a><a id="DESCRIPTION"></a><dl>
<dt><b>Description</b></dt>
</dl>
</td>
<td width="60%">
Descriptive comment about the server (replaces obsolete "Comment").

</td>
</tr>
<tr>
<td width="40%"><a id="ExchangeCertificate"></a><a id="exchangecertificate"></a><a id="EXCHANGECERTIFICATE"></a><dl>
<dt><b>ExchangeCertificate</b></dt>
</dl>
</td>
<td width="60%">
Name of the file that contains the exchange certificate (applies to Certificate Services 1.0 only).

</td>
</tr>
<tr>
<td width="40%"><a id="Flags"></a><a id="flags"></a><a id="FLAGS"></a><dl>
<dt><b>Flags</b></dt>
</dl>
</td>
<td width="60%">
String that represents the location where the CA information was found. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="Locality"></a><a id="locality"></a><a id="LOCALITY"></a><dl>
<dt><b>Locality</b></dt>
</dl>
</td>
<td width="60%">
City or town.

</td>
</tr>
<tr>
<td width="40%"><a id="Organization"></a><a id="organization"></a><a id="ORGANIZATION"></a><dl>
<dt><b>Organization</b></dt>
</dl>
</td>
<td width="60%">
Organization.

</td>
</tr>
<tr>
<td width="40%"><a id="OrgUnit"></a><a id="orgunit"></a><a id="ORGUNIT"></a><dl>
<dt><b>OrgUnit</b></dt>
</dl>
</td>
<td width="60%">
Organizational unit.

</td>
</tr>
<tr>
<td width="40%"><a id="SanitizedName"></a><a id="sanitizedname"></a><a id="SANITIZEDNAME"></a><dl>
<dt><b>SanitizedName</b></dt>
</dl>
</td>
<td width="60%">
CA name that is <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">sanitized</a> according to the rules described in 
<a href="https://msdn.microsoft.com/en-us/library/Aa383274(v=VS.85).aspx">GetConfig</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SanitizedShortName"></a><a id="sanitizedshortname"></a><a id="SANITIZEDSHORTNAME"></a><dl>
<dt><b>SanitizedShortName</b></dt>
</dl>
</td>
<td width="60%">
CA name that is sanitized and shortened according to the rules described in 
<a href="https://msdn.microsoft.com/en-us/library/Aa383274(v=VS.85).aspx">GetConfig</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="Server"></a><a id="server"></a><a id="SERVER"></a><dl>
<dt><b>Server</b></dt>
</dl>
</td>
<td width="60%">
Reference computer name.

</td>
</tr>
<tr>
<td width="40%"><a id="ShortName"></a><a id="shortname"></a><a id="SHORTNAME"></a><dl>
<dt><b>ShortName</b></dt>
</dl>
</td>
<td width="60%">
SanitizedShortName, but with the '!xxx' sequences, as described in 
<a href="https://msdn.microsoft.com/en-us/library/Aa383274(v=VS.85).aspx">GetConfig</a>, translated back into the original text.

</td>
</tr>
<tr>
<td width="40%"><a id="SignatureCertificate"></a><a id="signaturecertificate"></a><a id="SIGNATURECERTIFICATE"></a><dl>
<dt><b>SignatureCertificate</b></dt>
</dl>
</td>
<td width="60%">
Name of the file that contains the CA certificate (also known as the CA <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">signature certificate</a>); this may or may not be a <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">root certificate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="State"></a><a id="state"></a><a id="STATE"></a><dl>
<dt><b>State</b></dt>
</dl>
</td>
<td width="60%">
State or province.

</td>
</tr>
<tr>
<td width="40%"><a id="WebEnrollmentServers"></a><a id="webenrollmentservers"></a><a id="WEBENROLLMENTSERVERS"></a><dl>
<dt><b>WebEnrollmentServers</b></dt>
</dl>
</td>
<td width="60%">
An array of certificate enrollment Web service URLs for a specific CA configuration in the Active Directory.

<b>Windows Vista and Windows Storage Server 2003:  </b>This field is not supported.

</td>
</tr>
</table>
 


### -param pstrOut

TBD




#### - pbstrOut [out, retval]

A pointer to a <b>BSTR</b> that receives the data from the field. When you have finished using the <b>BSTR</b>, free <i>pbstrOut</i> by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that represents the data for the field.




## -remarks



This method returns the field data for the specified field.

When you specify "Flags" in the <i>strFieldName</i> parameter, the retrieved data for the flags field is a string that can be converted to an integer by means of the C-library function <b>_wtoi</b>. The resulting integer represents a bitfield that can be examined to determine whether the flags CAIF_DSENTRY and CAIF_SHAREDFOLDERENTRY are set. If CAIF_DSENTRY (0x00000001) is set, the information for the CA was contained in Directory Services. If CAIF_SHAREDFOLDERENTRY (0x00000002) is set, the information for the CA was contained in the shared folder. Note that one or both of these flags may be set.


#### Examples


```cpp
    BSTR  bstrFieldName = NULL;
    BSTR  bstrFieldValue = NULL;
    HRESULT    hr;

    // Specify the field to retrieve, for example, "CommonName".
    bstrFieldName = SysAllocString(L"<FIELDNAMEHERE>");
    if (NULL == bstrFieldName)
    {
        printf("Memory allocation failed for bstrFieldName.\n");
        goto error;
    }

    // pConfig is a previously instantiated ICertConfig object.
    hr = pConfig->GetField(bstrFieldName, &bstrFieldValue);
    if (FAILED(hr))
    {
        printf("Failed GetField - [%x]\n", hr);
        goto error;
    }
    else
        printf("GetField value for %ws is: %ws\n", 
            bstrFieldName, bstrFieldValue );

error:

    if (bstrFieldName)
        SysFreeString(bstrFieldName);

    if (bstrFieldValue)
        SysFreeString(bstrFieldValue);
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">CCertConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>
 

 


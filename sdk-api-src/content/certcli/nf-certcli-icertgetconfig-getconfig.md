---
UID: NF:certcli.ICertGetConfig.GetConfig
title: ICertGetConfig::GetConfig
author: windows-sdk-content
description: The ICertGetConfig::GetConfig method retrieves the configuration string for a Certificate Services server.
old-location: security\icertgetconfig_getconfig.htm
tech.root: seccrypto
ms.assetid: 5935bf37-4a4a-4c0f-ae3f-bd76f97d0d9a
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CC_DEFAULTCONFIG, CC_FIRSTCONFIG, CC_LOCALACTIVECONFIG, CC_LOCALCONFIG, CC_UIPICKCONFIG, CC_UIPICKCONFIGSKIPLOCALCA, GetConfig, GetConfig method [Security], GetConfig method [Security],ICertGetConfig interface, ICertGetConfig interface [Security],GetConfig method, ICertGetConfig.GetConfig, ICertGetConfig::GetConfig, certcli/ICertGetConfig::GetConfig, security.icertgetconfig_getconfig
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
 - ICertGetConfig.GetConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertGetConfig::GetConfig


## -description


The <b>GetConfig</b> method retrieves the configuration string for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> server.
			

The configuration string is the server name and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) name separated by a backslash (\); for example: <i>ServerName</i>\<i>CAName</i>. This configuration string can be used to refer unambiguously to a specific Certificate Services server. For more information, see Remarks.


## -parameters




### -param Flags [in]

Value that specifies the CA to use. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CC_DEFAULTCONFIG"></a><a id="cc_defaultconfig"></a><dl>
<dt><b>CC_DEFAULTCONFIG</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Retrieves the default CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_FIRSTCONFIG"></a><a id="cc_firstconfig"></a><dl>
<dt><b>CC_FIRSTCONFIG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns the first CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_LOCALACTIVECONFIG"></a><a id="cc_localactiveconfig"></a><dl>
<dt><b>CC_LOCALACTIVECONFIG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Retrieves the local CA if it is running.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_LOCALCONFIG"></a><a id="cc_localconfig"></a><dl>
<dt><b>CC_LOCALCONFIG</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Retrieves the local CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_UIPICKCONFIG"></a><a id="cc_uipickconfig"></a><dl>
<dt><b>CC_UIPICKCONFIG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Displays a user interface (UI) that allows the user to select a CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_UIPICKCONFIGSKIPLOCALCA_"></a><a id="cc_uipickconfigskiplocalca_"></a><dl>
<dt><b>CC_UIPICKCONFIGSKIPLOCALCA </b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Displays a UI that allows the user to select a CA. The UI excludes any local CA. This exclusion is useful during subordinate CA certificate renewal when the subordinate CA certificate request is submitted to a CA other than the current CA.

</td>
</tr>
</table>
 


### -param pstrOut

TBD




#### - pbstrOut [out]

A pointer to a <b>BSTR</b> that contains the configuration. When you have finished using the configuration, call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to free <i>pbstrOut</i>.


## -returns



If the function is successful, the return value is S_OK.

 
If the method fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) name portion of the configuration string that this function returns is the exact text entered during the Certificate Services setup process. Note that this text may be different from the form of the CA name found in file names (such as for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a>) or in registry keys. This is because file names and registry keys use a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">sanitized</a> version of the CA name.

The process of sanitizing the CA name is necessary to remove characters that are illegal for file names, registry key names, or distinguished name values, or illegal for reasons specific to Certificate Services. In the sanitizing process, any illegal character in the common name is converted to a five-character representation in the format <b>!</b><i>xxxx</i>, where the exclamation point (<b>!</b>) is used as an escape character and <i>xxxx</i> represents four hexadecimal digits that uniquely identify the character to be converted.

For example, the number sign (#) is not allowed in distinguished names in the Active Directory directory service. If the CA name entered during setup is <b>#</b><i>YourName</i>, the sanitized CA name will be <b>!0023</b><i>YourName</i>.

The following characters, if entered for the common name of the CA during setup, are converted to the <b>!</b><i>xxxx</i> format during the sanitizing process. This list is subject to change.

<table>
<tr>
<th>Character</th>
<th>Value in !xxxx format</th>
</tr>
<tr>
<td>&lt;</td>
<td>!003c</td>
</tr>
<tr>
<td>&gt;</td>
<td>!003e</td>
</tr>
<tr>
<td>"</td>
<td>!0022</td>
</tr>
<tr>
<td>/</td>
<td>!002f</td>
</tr>
<tr>
<td>\</td>
<td>!005c</td>
</tr>
<tr>
<td>:</td>
<td>!003a</td>
</tr>
<tr>
<td>|</td>
<td>!007c</td>
</tr>
<tr>
<td>?</td>
<td>!003f</td>
</tr>
<tr>
<td>*</td>
<td>!002a</td>
</tr>
<tr>
<td>#</td>
<td>!0023</td>
</tr>
<tr>
<td>,</td>
<td>!002c</td>
</tr>
<tr>
<td>+</td>
<td>!002b</td>
</tr>
<tr>
<td>;</td>
<td>!003b</td>
</tr>
<tr>
<td>!</td>
<td>!0021</td>
</tr>
</table>
 

Any nonprinting character and all <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> characters that are not seven bits are also converted to the <b>!</b><i>xxxx</i> format.

A sanitized short name is generated when the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">sanitized name</a> is too long for a 64-character directory services <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative distinguished name</a> (RDN). The sanitized short name consists of the sanitized name truncated and appended with a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the full sanitized name. The sanitized short name reserves some of the 64 characters to contain <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) suffixes, such as (123).

The CA name portion of the configuration string returned by this method is the original text entered during setup. Note that Certificate Services methods that require a CA name as a parameter accept the originally entered CA name. For example, for the CA name <b>#</b><i>YourName</i>, the  
<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">ICertView2::OpenConnection</a> method accepts <b>#</b><i>YourName</i> as the parameter's CA portion.




## -see-also




<a href="https://msdn.microsoft.com/3a35b2a0-f8e4-496d-b76a-a7310842cc4c">ICertConfig2::GetConfig</a>



<a href="https://msdn.microsoft.com/753d1527-1863-41af-9715-2c1fe138e67d">ICertGetConfig</a>



<a href="https://msdn.microsoft.com/576af4d1-88c9-40e3-9438-9fefd483be7a">ICertView2::OpenConnection</a>
 

 


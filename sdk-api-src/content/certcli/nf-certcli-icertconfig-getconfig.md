---
UID: NF:certcli.ICertConfig.GetConfig
title: ICertConfig::GetConfig (certcli.h)
description: Retrieves the configuration string for a Certificate Services server. This method was first defined in the ICertConfig interface.
helpviewer_keywords: ["CC_DEFAULTCONFIG","CC_FIRSTCONFIG","CC_LOCALACTIVECONFIG","CC_LOCALCONFIG","CC_UIPICKCONFIG","CC_UIPICKCONFIGSKIPLOCALCA","CCertConfig object [Security]","GetConfig method","GetConfig","GetConfig method [Security]","GetConfig method [Security]","CCertConfig object","GetConfig method [Security]","ICertConfig interface","GetConfig method [Security]","ICertConfig2 interface","ICertConfig interface [Security]","GetConfig method","ICertConfig.GetConfig","ICertConfig2 interface [Security]","GetConfig method","ICertConfig2::GetConfig","ICertConfig::GetConfig","_certsrv_icertconfig_getconfig","certcli/ICertConfig2::GetConfig","certcli/ICertConfig::GetConfig","security.icertconfig2_getconfig"]
old-location: security\icertconfig2_getconfig.htm
tech.root: security
ms.assetid: 3a35b2a0-f8e4-496d-b76a-a7310842cc4c
ms.date: 12/05/2018
ms.keywords: CC_DEFAULTCONFIG, CC_FIRSTCONFIG, CC_LOCALACTIVECONFIG, CC_LOCALCONFIG, CC_UIPICKCONFIG, CC_UIPICKCONFIGSKIPLOCALCA, CCertConfig object [Security],GetConfig method, GetConfig, GetConfig method [Security], GetConfig method [Security],CCertConfig object, GetConfig method [Security],ICertConfig interface, GetConfig method [Security],ICertConfig2 interface, ICertConfig interface [Security],GetConfig method, ICertConfig.GetConfig, ICertConfig2 interface [Security],GetConfig method, ICertConfig2::GetConfig, ICertConfig::GetConfig, _certsrv_icertconfig_getconfig, certcli/ICertConfig2::GetConfig, certcli/ICertConfig::GetConfig, security.icertconfig2_getconfig
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
targetos: Windows
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertConfig::GetConfig
 - certcli/ICertConfig::GetConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig2.GetConfig
 - ICertConfig.GetConfig
 - CCertConfig.GetConfig
---

# ICertConfig::GetConfig


## -description

The <b>GetConfig</b> method retrieves the configuration string for a <a href="/windows/desktop/SecGloss/c-gly">Certificate Services</a> server. This method was first defined in the <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a> interface.

The configuration string is the server name and <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> name separated by a backslash (\\); for example: <i>ServerName</i><b>\\</b><i>CAName</i>. This configuration string can be used to refer unambiguously to a specific Certificate Services server. For more information, see Remarks.

## -parameters

### -param Flags [in]

Value that specifies the certification authority to use. This parameter can be one of the  following values.

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
Retrieves the default certification authority.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_FIRSTCONFIG"></a><a id="cc_firstconfig"></a><dl>
<dt><b>CC_FIRSTCONFIG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns the first certification authority.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_LOCALACTIVECONFIG"></a><a id="cc_localactiveconfig"></a><dl>
<dt><b>CC_LOCALACTIVECONFIG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Retrieves the local certification authority if it is running.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_LOCALCONFIG"></a><a id="cc_localconfig"></a><dl>
<dt><b>CC_LOCALCONFIG</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Retrieves the local certification authority.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_UIPICKCONFIG"></a><a id="cc_uipickconfig"></a><dl>
<dt><b>CC_UIPICKCONFIG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Displays a user interface that allows the user to select a certification authority.

</td>
</tr>
<tr>
<td width="40%"><a id="CC_UIPICKCONFIGSKIPLOCALCA_"></a><a id="cc_uipickconfigskiplocalca_"></a><dl>
<dt><b>CC_UIPICKCONFIGSKIPLOCALCA </b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Displays a user interface that allows the user to select a certification authority. The UI excludes any local certification authority. This exclusion is useful during subordinate certification authority certificate renewal when the subordinate certification authority certificate request is submitted to a certification authority other than the current certification authority.

</td>
</tr>
</table>

### -param pstrOut [out]

A pointer to a <b>BSTR</b> that contains the configuration. When you have finished using the configuration, call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to free <i>pbstrOut</i>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that contains the configuration.

## -remarks

The <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) name portion of the configuration string that this function returns is the exact text entered during the Certificate Services setup process. Note that this text may be different from the form of the CA name found in file names (such as for the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a>) or in registry keys. This is because file names and registry keys use a <a href="/windows/desktop/SecGloss/s-gly">sanitized</a> version of the CA name.

The process of sanitizing the CA name is necessary to remove characters that are illegal for file names, registry key names, or distinguished name values, or illegal for reasons specific to Certificate Services. In the sanitizing process, any illegal character in the common name is converted to a five-character representation in the format <b>!</b><i>xxxx</i>, where <b>!</b> is used as an escape character and <i>xxxx</i> represents four hexadecimal digits that uniquely identify the character to be converted.

For example, the number sign (#) is not allowed in distinguished names in Active Directory. If the CA name entered during setup is <b>#</b><i>YourName</i>, the sanitized CA name will be <b>!0023</b><i>YourName</i>.

The following characters, if entered for the common name of the CA during setup, are converted to the <b>!</b><i>xxxx</i> format during the sanitizing process. This list is subject to change.

<table>
<tr>
<th>Name</th>
<th>Character</th>
<th>Value in !xxxx format</th>
</tr>
<tr>
<td>Ampersand</td>
<td>&amp;</td>
<td>!0026</td>
</tr>
<tr>
<td>Apostrophe</td>
<td>'</td>
<td>!0027</td>
</tr>
<tr>
<td>Asterisk</td>
<td>*</td>
<td>!002a</td>
</tr>
<tr>
<td>Backslash</td>
<td>\</td>
<td>!005c</td>
</tr>
<tr>
<td>Left brace</td>
<td>{</td>
<td>!007b</td>
</tr>
<tr>
<td>Right brace</td>
<td>}</td>
<td>!007d</td>
</tr>
<tr>
<td>Left bracket</td>
<td>[</td>
<td>!005b</td>
</tr>
<tr>
<td>Right bracket</td>
<td>]</td>
<td>!005d</td>
</tr>
<tr>
<td>Caret</td>
<td>^</td>
<td>!005e</td>
</tr>
<tr>
<td>Colon</td>
<td>:</td>
<td>!003a</td>
</tr>
<tr>
<td>Comma</td>
<td>,</td>
<td>!002c</td>
</tr>
<tr>
<td>Equal sign</td>
<td>=</td>
<td>!003d</td>
</tr>
<tr>
<td>Exclamation point</td>
<td>!</td>
<td>!0021</td>
</tr>
<tr>
<td>Grave accent</td>
<td>`</td>
<td>!0060</td>
</tr>
<tr>
<td>Greater than sign</td>
<td>&gt;</td>
<td>!003e</td>
</tr>
<tr>
<td>Less than sign</td>
<td>&lt;</td>
<td>!003c</td>
</tr>
<tr>
<td>Number sign</td>
<td>#</td>
<td>!0023</td>
</tr>
<tr>
<td>Opening parenthesis</td>
<td>(</td>
<td>!0028</td>
</tr>
<tr>
<td>Closing parenthesis</td>
<td>)</td>
<td>!0029</td>
</tr>
<tr>
<td>Percent</td>
<td>%</td>
<td>!0025</td>
</tr>
<tr>
<td>Pipe</td>
<td>|</td>
<td>!007c</td>
</tr>
<tr>
<td>Plus sign</td>
<td>+</td>
<td>!002b</td>
</tr>
<tr>
<td>Question mark</td>
<td>?</td>
<td>!003f</td>
</tr>
<tr>
<td>Quotation mark</td>
<td>"</td>
<td>!0022</td>
</tr>
<tr>
<td>Semicolon</td>
<td>;</td>
<td>!003b</td>
</tr>
<tr>
<td>Slash mark</td>
<td>/</td>
<td>!002f</td>
</tr>
</table>
 

Any nonprinting character and all <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> characters that are not seven bits are also converted to the <b>!</b><i>xxxx</i> format.

A sanitized short name is generated when the <a href="/windows/desktop/SecGloss/s-gly">sanitized name</a> is too long for a 64-character directory services <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN). The sanitized short name consists of the sanitized name truncated and appended with a <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the full sanitized name. The sanitized short name reserves some of the 64 characters to contain <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) suffixes, such as (123).

The certification authority name portion of the configuration string returned by this method is the original text entered during setup. Note that Certificate Services methods that require a certification authority name as a parameter accept the originally entered certification authority name. For example, for the certification authority name <b>#</b><i>YourName</i>, the  
<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView2::OpenConnection</a> method accepts <b>#</b><i>YourName</i> as the parameter's certification authority portion.


#### Examples

The following example shows how to use this method to retrieve the default certification authority configuration string.


```cpp

    ICertConfig2 * pConfig = NULL;
    BSTR  bstrConfig = NULL; //Contains CA configuration name
    HRESULT    hr;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx - [%x]\n", hr);
        goto error;
    }

    // Create an instance of the CertConfig object.
    hr = CoCreateInstance( CLSID_CCertConfig,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertConfig2,
                           (void **)&pConfig);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance - pConfig [%x]\n", hr);
        goto error;
    }

    // Retrieve the default CA configuration string.
    hr = pConfig->GetConfig(CC_DEFAULTCONFIG, &bstrConfig);
    if (FAILED(hr))
    {
        printf("Failed GetConfig - [%x]\n", hr);
        goto error;
    }
    else
        printf("GetConfig returned: %ws\n", bstrConfig );

error:

    // Done processing.
    if (pConfig)
        pConfig->Release();

    if (bstrConfig)
        SysFreeString(bstrConfig);

    CoUninitialize();

```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig2">CCertConfig</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openconnection">ICertView2::OpenConnection</a>
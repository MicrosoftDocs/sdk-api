---
UID: NF:winbio.WinBioGetDomainLogonSetting
title: WinBioGetDomainLogonSetting function (winbio.h)
description: Retrieves a value that specifies whether users can log on to a domain by using biometric information.
helpviewer_keywords: ["WINBIO_SETTING_SOURCE_DEFAULT","WINBIO_SETTING_SOURCE_INVALID","WINBIO_SETTING_SOURCE_LOCAL","WINBIO_SETTING_SOURCE_POLICY","WinBioGetDomainLogonSetting","WinBioGetDomainLogonSetting function [Windows Biometric Framework API]","secbiomet.winbiogetdomainlogonsetting","winbio/WinBioGetDomainLogonSetting"]
old-location: secbiomet\winbiogetdomainlogonsetting.htm
tech.root: SecBioMet
ms.assetid: bc09c606-654e-4871-ae2e-09fac3982e94
ms.date: 12/05/2018
ms.keywords: WINBIO_SETTING_SOURCE_DEFAULT, WINBIO_SETTING_SOURCE_INVALID, WINBIO_SETTING_SOURCE_LOCAL, WINBIO_SETTING_SOURCE_POLICY, WinBioGetDomainLogonSetting, WinBioGetDomainLogonSetting function [Windows Biometric Framework API], secbiomet.winbiogetdomainlogonsetting, winbio/WinBioGetDomainLogonSetting
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioGetDomainLogonSetting
 - winbio/WinBioGetDomainLogonSetting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - Winbio.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - winbioext.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioGetDomainLogonSetting
---

# WinBioGetDomainLogonSetting function


## -description

Retrieves a value that specifies whether users can log on to a domain by using biometric information.

## -parameters

### -param Value [out]

Pointer to a Boolean value that specifies whether biometric domain logons are enabled.

### -param Source [out]

Pointer to a <b>WINBIO_SETTING_SOURCE_TYPE</b> value that specifies the setting source. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_INVALID"></a><a id="winbio_setting_source_invalid"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The setting is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_DEFAULT"></a><a id="winbio_setting_source_default"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The setting originated from built-in policy.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_LOCAL"></a><a id="winbio_setting_source_local"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The setting originated in  the local computer registry.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_POLICY"></a><a id="winbio_setting_source_policy"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The setting was created by Group Policy.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/SecBioMet/client-application-functions">Client Application Functions</a>
---
UID: NF:sspi.SetContextAttributesW
title: SetContextAttributesW function (sspi.h)
description: Enables a transport application to set attributes of a security context for a security package. This function is supported only by the Schannel security package. (Unicode)
helpviewer_keywords: ["SECPKG_ATTR_APP_DATA", "SECPKG_ATTR_DTLS_MTU", "SECPKG_ATTR_EAP_PRF_INFO", "SECPKG_ATTR_EARLY_START", "SECPKG_ATTR_KEYING_MATERIAL_INFO", "SetContextAttributes", "SetContextAttributes function [Security]", "SetContextAttributesW", "security.setcontextattributes", "sspi/SetContextAttributes", "sspi/SetContextAttributesW"]
old-location: security\setcontextattributes.htm
tech.root: security
ms.assetid: e3246c3e-3e8c-49fe-99d8-dfff1a10ab83
ms.date: 12/05/2018
ms.keywords: SECPKG_ATTR_APP_DATA, SECPKG_ATTR_DTLS_MTU, SECPKG_ATTR_EAP_PRF_INFO, SECPKG_ATTR_EARLY_START, SECPKG_ATTR_KEYING_MATERIAL_INFO, SetContextAttributes, SetContextAttributes function [Security], SetContextAttributesA, SetContextAttributesW, security.setcontextattributes, sspi/SetContextAttributes, sspi/SetContextAttributesA, sspi/SetContextAttributesW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetContextAttributesW (Unicode) and SetContextAttributesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetContextAttributesW
 - sspi/SetContextAttributesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - SetContextAttributes
 - SetContextAttributesA
 - SetContextAttributesW
---

# SetContextAttributesW function


## -description

Enables a transport application to set  <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of a security <a href="/windows/desktop/SecGloss/c-gly">context</a> for a <a href="/windows/desktop/SecGloss/s-gly">security package</a>. This function is supported only by the Schannel security package.

## -parameters

### -param phContext [in]

A handle to the security context to be set.

### -param ulAttribute [in]

The attribute of the context to be set. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_APP_DATA"></a><a id="secpkg_attr_app_data"></a><dl>
<dt><b>SECPKG_ATTR_APP_DATA</b></dt>
<dt>94</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_sessionappdata">SecPkgContext_SessionAppData</a> structure.

Sets application data for the session.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_EAP_PRF_INFO"></a><a id="secpkg_attr_eap_prf_info"></a><dl>
<dt><b>SECPKG_ATTR_EAP_PRF_INFO</b></dt>
<dt>101</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_eapprfinfo">SecPkgContext_EapPrfInfo</a> structure.

Sets the pseudo-random function (PRF) used by the Extensible Authentication Protocol (EAP). This is the value that is returned by a call to the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes (Schannel)</a> function when <b>SECPKG_ATTR_EAP_KEY_BLOCK</b> is passed as the value of the <i>ulAttribute</i> parameter.

This attribute is supported only by the Schannel security package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_EARLY_START"></a><a id="secpkg_attr_early_start"></a><dl>
<dt><b>SECPKG_ATTR_EARLY_START</b></dt>
<dt>105</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_earlystart">SecPkgContext_EarlyStart</a> structure.

Sets the False Start feature. See  the <a href="/windows/desktop/winmsg/windows">Building a faster and more secure web</a> blog post for information on this feature.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_DTLS_MTU"></a><a id="secpkg_attr_dtls_mtu"></a><dl>
<dt><b>SECPKG_ATTR_DTLS_MTU</b></dt>
<dt>34</dt>
</dl>
</td>
<td width="60%">
Sets and retrieves the MTU (maximum transmission unit) value for use with DTLS. 
If DTLS is not enabled in a security context, this attribute is not supported. 


Valid values are between 200 bytes and 64 kilobytes. The default DTLS MTU value in Schannel is 1096 bytes. 


</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_ATTR_KEYING_MATERIAL_INFO"></a><a id="secpkg_attr_keying_material_info"></a><dl>
<dt><b>SECPKG_ATTR_KEYING_MATERIAL_INFO</b></dt>
<dt>106</dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter contains a pointer to a <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_keyingmaterialinfo">SecPkgContext_KeyingMaterialInfo</a> structure. The keying material export feature follows the <a href="https://tools.ietf.org/html/rfc5705">RFC 5705 standard</a>.

This attribute is supported only by the Schannel security package in Windows 10 and Windows Server 2016 or later versions.

</td>
</tr>
</table>

### -param pBuffer [in]

A pointer to a structure that contains  values to set  the attributes to. The type of structure pointed to depends on the value specified in the <i>ulAttribute</i> parameter.

### -param cbBuffer [in]

The size, in bytes, of the <i>pBuffer</i> parameter.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code. The following error code is one of the possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
This value is returned by Schannel kernel mode to indicate that this function is not supported.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The sspi.h header defines SetContextAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

---
UID: NF:adshlp.SecurityDescriptorToBinarySD
title: SecurityDescriptorToBinarySD function (adshlp.h)
description: Converts an IADsSecurityDescriptor object to the binary security descriptor format.
helpviewer_keywords: ["SecurityDescriptorToBinarySD","SecurityDescriptorToBinarySD function [ADSI]","adshlp/SecurityDescriptorToBinarySD","adsi.securitydescriptortobinarysd"]
old-location: adsi\securitydescriptortobinarysd.htm
tech.root: adsi
ms.assetid: b1c814fd-df0f-406b-adfc-c356ce37d524
ms.date: 12/05/2018
ms.keywords: SecurityDescriptorToBinarySD, SecurityDescriptorToBinarySD function [ADSI], adshlp/SecurityDescriptorToBinarySD, adsi.securitydescriptortobinarysd
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SecurityDescriptorToBinarySD
 - adshlp/SecurityDescriptorToBinarySD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - SecurityDescriptorToBinarySD
---

# SecurityDescriptorToBinarySD function


## -description

The <b>SecurityDescriptorToBinarySD</b> function converts an <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object to the binary security descriptor format.

## -parameters

### -param vVarSecDes [in]

Type: <b>VARIANT</b>

Contains a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that contains the security descriptor to convert. The <b>VARIANT</b> must contain a <b>VT_DISPATCH</b> that contains an <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

### -param ppSecurityDescriptor [out]

Type: <b>PSECURITY_DESCRIPTOR*</b>

Address of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> pointer that receives the binary security descriptor data. The caller must free this memory by passing this pointer to the <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> function.

### -param pdwSDLength [out]

Type: <b>PDWORD</b>

Address of a <b>DWORD</b> value that receives the length, in bytes of the binary security descriptor data.

### -param pszServerName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that specifies the name of the server where the security descriptor is placed. This parameter is optional and can be <b>NULL</b>.

### -param userName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that contains the user name that the security descriptor is associated to. This parameter is optional and can be <b>NULL</b>.

### -param passWord [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that contains the password that the security descriptor is associated. This parameter is optional and can be <b>NULL</b>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Contains authentication flags for the conversion. This can be zero or a combination of one or more of the <a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a> enumeration values.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values, as well as the following.

## -remarks

This function is used for legacy applications to manually convert security descriptors to binary security descriptors. For new applications, use <a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>, which performs this conversion automatically.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-binarysdtosecuritydescriptor">BinarySDToSecurityDescriptor</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>
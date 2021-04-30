---
UID: NF:adshlp.BinarySDToSecurityDescriptor
title: BinarySDToSecurityDescriptor function (adshlp.h)
description: Converts a binary security descriptor to an IADsSecurityDescriptor object.
helpviewer_keywords: ["BinarySDToSecurityDescriptor","BinarySDToSecurityDescriptor function [ADSI]","adshlp/BinarySDToSecurityDescriptor","adsi.binarysdtosecuritydescriptor"]
old-location: adsi\binarysdtosecuritydescriptor.htm
tech.root: adsi
ms.assetid: c93d00d2-7155-4bf4-8a65-2412022a2fba
ms.date: 12/05/2018
ms.keywords: BinarySDToSecurityDescriptor, BinarySDToSecurityDescriptor function [ADSI], adshlp/BinarySDToSecurityDescriptor, adsi.binarysdtosecuritydescriptor
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
 - BinarySDToSecurityDescriptor
 - adshlp/BinarySDToSecurityDescriptor
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
 - BinarySDToSecurityDescriptor
---

# BinarySDToSecurityDescriptor function


## -description

The <b>BinarySDToSecurityDescriptor</b> function converts a binary security descriptor to an <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

## -parameters

### -param pSecurityDescriptor [in]

Type: <b>PSECURITY_DESCRIPTOR</b>

Address of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure to convert.

### -param pVarsec [out]

Type: <b>VARIANT*</b>

Address of a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that receives the object. The <b>VARIANT</b> contains a <b>VT_DISPATCH</b> object that can be queried for the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface. The caller must release this <b>VARIANT</b> by passing the <b>VARIANT</b> to the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> function.

### -param pszServerName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the name of the server that the security descriptor was retrieved from. This parameter is optional and can be <b>NULL</b>.

### -param userName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the user name to be associated with the security descriptor. This parameter is optional and can be <b>NULL</b>.

### -param passWord [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the password to be associated with the security descriptor. This parameter is optional and can be <b>NULL</b>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Contains authentication flags for the conversion. This can be zero or a combination of one or more of the <a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a> enumeration values.

## -returns

Type: <b>HRESULT</b>

This method supports  standard return values, as well as the following:

If the operation fails, an ADSI error code is returned. For more information, see <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This function is used for legacy applications that must  manually convert security descriptors to binary security descriptors. For new applications, use the <a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a> interface, which does this conversion automatically.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-securitydescriptortobinarysd">SecurityDescriptorToBinarySD</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>
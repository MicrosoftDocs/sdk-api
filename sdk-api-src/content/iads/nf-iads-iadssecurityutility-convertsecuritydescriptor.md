---
UID: NF:iads.IADsSecurityUtility.ConvertSecurityDescriptor
title: IADsSecurityUtility::ConvertSecurityDescriptor (iads.h)
description: Converts a security descriptor from one format to another.
helpviewer_keywords: ["ADS_SD_FORMAT_HEXSTRING","ADS_SD_FORMAT_IID","ADS_SD_FORMAT_RAW","ConvertSecurityDescriptor","ConvertSecurityDescriptor method [ADSI]","ConvertSecurityDescriptor method [ADSI]","IADsSecurityUtility interface","IADsSecurityUtility interface [ADSI]","ConvertSecurityDescriptor method","IADsSecurityUtility.ConvertSecurityDescriptor","IADsSecurityUtility::ConvertSecurityDescriptor","_ds_iadssecurityutility_convertsecuritydescriptor","adsi.iadssecurityutility__convertsecuritydescriptor","adsi.iadssecurityutility_convertsecuritydescriptor","iads/IADsSecurityUtility::ConvertSecurityDescriptor"]
old-location: adsi\iadssecurityutility_convertsecuritydescriptor.htm
tech.root: adsi
ms.assetid: ea6509bd-5625-458b-be7a-abb43ba2f46e
ms.date: 12/05/2018
ms.keywords: ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, ConvertSecurityDescriptor, ConvertSecurityDescriptor method [ADSI], ConvertSecurityDescriptor method [ADSI],IADsSecurityUtility interface, IADsSecurityUtility interface [ADSI],ConvertSecurityDescriptor method, IADsSecurityUtility.ConvertSecurityDescriptor, IADsSecurityUtility::ConvertSecurityDescriptor, _ds_iadssecurityutility_convertsecuritydescriptor, adsi.iadssecurityutility__convertsecuritydescriptor, adsi.iadssecurityutility_convertsecuritydescriptor, iads/IADsSecurityUtility::ConvertSecurityDescriptor
req.header: iads.h
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsSecurityUtility::ConvertSecurityDescriptor
 - iads/IADsSecurityUtility::ConvertSecurityDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility.ConvertSecurityDescriptor
---

# IADsSecurityUtility::ConvertSecurityDescriptor


## -description

The <b>ConvertSecurityDescriptor</b> method converts a security descriptor from one format to another.

## -parameters

### -param varSD [in]

A <b>VARIANT</b> that contains the security descriptor to convert. The format of this <b>VARIANT</b> is defined  by the <i>lDataFormat</i> parameter.

### -param lDataFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor in the <i>varSD</i> parameter. The following list identifies the possible values for this parameter and the format of the <i>varSD</i> parameter.



#### ADS_SD_FORMAT_IID

<i>varSD</i> contains a <b>VT_DISPATCH</b> that can be queried for the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>varSD</i> contains a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>varSD</i> contains a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.

### -param lOutFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a> values which specifies the format that the security descriptor should be converted to. The following list identifies the possible values for this parameter and the format of the <i>pvResult</i> parameter.



#### ADS_SD_FORMAT_IID

<i>pvResult</i> receives a <b>VT_DISPATCH</b> that can be queried for the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>pvResult</i> receives a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>pvResult</i> receives a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.

### -param pResult [out]

Pointer to a <b>VARIANT</b> that receives the converted security descriptor. The format of the retrieved security descriptor is specified by the <i>lOutFormat</i> parameter.

## -returns

Returns <b>S_OK</b> if successful or a COM or Win32 error code otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>
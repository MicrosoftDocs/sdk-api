---
UID: NF:iads.IADsSecurityUtility.GetSecurityDescriptor
title: IADsSecurityUtility::GetSecurityDescriptor (iads.h)
description: Retrieves a security descriptor for the specified file, fileshare, or registry key.
helpviewer_keywords: ["ADS_SD_FORMAT_HEXSTRING","ADS_SD_FORMAT_IID","ADS_SD_FORMAT_RAW","File","File share","GetSecurityDescriptor","GetSecurityDescriptor method [ADSI]","GetSecurityDescriptor method [ADSI]","IADsSecurityUtility interface","IADsSecurityUtility interface [ADSI]","GetSecurityDescriptor method","IADsSecurityUtility.GetSecurityDescriptor","IADsSecurityUtility::GetSecurityDescriptor","Registry key","_ds_iadssecurityutility_getsecuritydescriptor","adsi.iadssecurityutility__getsecuritydescriptor","adsi.iadssecurityutility_getsecuritydescriptor","iads/IADsSecurityUtility::GetSecurityDescriptor"]
old-location: adsi\iadssecurityutility_getsecuritydescriptor.htm
tech.root: adsi
ms.assetid: 95f4fbd9-03f8-4f2f-9314-e628186e51a4
ms.date: 12/05/2018
ms.keywords: ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, File, File share, GetSecurityDescriptor, GetSecurityDescriptor method [ADSI], GetSecurityDescriptor method [ADSI],IADsSecurityUtility interface, IADsSecurityUtility interface [ADSI],GetSecurityDescriptor method, IADsSecurityUtility.GetSecurityDescriptor, IADsSecurityUtility::GetSecurityDescriptor, Registry key, _ds_iadssecurityutility_getsecuritydescriptor, adsi.iadssecurityutility__getsecuritydescriptor, adsi.iadssecurityutility_getsecuritydescriptor, iads/IADsSecurityUtility::GetSecurityDescriptor
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
 - IADsSecurityUtility::GetSecurityDescriptor
 - iads/IADsSecurityUtility::GetSecurityDescriptor
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
 - IADsSecurityUtility.GetSecurityDescriptor
---

# IADsSecurityUtility::GetSecurityDescriptor


## -description

The <b>GetSecurityDescriptor</b> method retrieves a security descriptor for the specified file, fileshare, or registry key.

## -parameters

### -param varPath [in]

A <b>VARIANT</b> string that contains the path of the object to retrieve the security descriptor for.



#### File

A valid file path syntax. For example: "c:\specs\public\adxml.doc" or "\\adsi\public\dsclient.exe".



#### File share

A valid file path syntax for a file share. For example: "\\adsi\public".



#### Registry key

A valid registry syntax. For example, "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ADs".

### -param lPathFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a> values which specifies the format of the <i>varPath</i> parameter.

### -param lFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor returned in the <i>pVariant</i> parameter. The following list identifies the possible values for this parameter and the format that is supplied in the <i>pVariant</i> parameter.



#### ADS_SD_FORMAT_IID

<i>pVariant</i> receives a <b>VT_DISPATCH</b> that can be queried for the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>pVariant</i> receives a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>pVariant</i> receives a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.

### -param pVariant [out]

Pointer to a <b>VARIANT</b> that receives the returned security descriptor. The format of the retrieved security descriptor is specified by the <i>lFormat</i> parameter.

## -returns

Returns <b>S_OK</b> if successful or a COM or Win32 error code otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor">SetSecurityDescriptor</a>
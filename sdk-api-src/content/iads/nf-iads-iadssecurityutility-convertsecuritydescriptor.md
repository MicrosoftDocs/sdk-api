---
UID: NF:iads.IADsSecurityUtility.ConvertSecurityDescriptor
title: IADsSecurityUtility::ConvertSecurityDescriptor
author: windows-sdk-content
description: Converts a security descriptor from one format to another.
old-location: adsi\iadssecurityutility_convertsecuritydescriptor.htm
old-project: ADSI
ms.assetid: ea6509bd-5625-458b-be7a-abb43ba2f46e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, ConvertSecurityDescriptor, ConvertSecurityDescriptor method [ADSI], ConvertSecurityDescriptor method [ADSI],IADsSecurityUtility interface, IADsSecurityUtility interface [ADSI],ConvertSecurityDescriptor method, IADsSecurityUtility.ConvertSecurityDescriptor, IADsSecurityUtility::ConvertSecurityDescriptor, _ds_iadssecurityutility_convertsecuritydescriptor, adsi.iadssecurityutility__convertsecuritydescriptor, adsi.iadssecurityutility_convertsecuritydescriptor, iads/IADsSecurityUtility::ConvertSecurityDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility.ConvertSecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsSecurityUtility::ConvertSecurityDescriptor


## -description


The <b>ConvertSecurityDescriptor</b> method converts a security descriptor from one format to another.


## -parameters




### -param varSD [in]

A <b>VARIANT</b> that contains the security descriptor to convert. The format of this <b>VARIANT</b> is defined  by the <i>lDataFormat</i> parameter.


### -param lDataFormat [in]

Contains one of the <a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor in the <i>varSD</i> parameter. The following list identifies the possible values for this parameter and the format of the <i>varSD</i> parameter.



#### ADS_SD_FORMAT_IID

<i>varSD</i> contains a <b>VT_DISPATCH</b> that can be queried for the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>varSD</i> contains a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>varSD</i> contains a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.


### -param lOutFormat [in]

Contains one of the <a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a> values which specifies the format that the security descriptor should be converted to. The following list identifies the possible values for this parameter and the format of the <i>pvResult</i> parameter.



#### ADS_SD_FORMAT_IID

<i>pvResult</i> receives a <b>VT_DISPATCH</b> that can be queried for the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>pvResult</i> receives a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>pvResult</i> receives a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.


### -param pResult






#### - pvResult [out]

Pointer to a <b>VARIANT</b> that receives the converted security descriptor. The format of the retrieved security descriptor is specified by the <i>lOutFormat</i> parameter.


## -returns



Returns <b>S_OK</b> if successful or a COM or Win32 error code otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>
 

 


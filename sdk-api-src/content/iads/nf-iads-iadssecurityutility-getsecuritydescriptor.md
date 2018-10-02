---
UID: NF:iads.IADsSecurityUtility.GetSecurityDescriptor
title: IADsSecurityUtility::GetSecurityDescriptor
author: windows-sdk-content
description: Retrieves a security descriptor for the specified file, fileshare, or registry key.
old-location: adsi\iadssecurityutility_getsecuritydescriptor.htm
tech.root: ADSI
ms.assetid: 95f4fbd9-03f8-4f2f-9314-e628186e51a4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, File, File share, GetSecurityDescriptor, GetSecurityDescriptor method [ADSI], GetSecurityDescriptor method [ADSI],IADsSecurityUtility interface, IADsSecurityUtility interface [ADSI],GetSecurityDescriptor method, IADsSecurityUtility.GetSecurityDescriptor, IADsSecurityUtility::GetSecurityDescriptor, Registry key, _ds_iadssecurityutility_getsecuritydescriptor, adsi.iadssecurityutility__getsecuritydescriptor, adsi.iadssecurityutility_getsecuritydescriptor, iads/IADsSecurityUtility::GetSecurityDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility.GetSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Contains one of the <a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a> values which specifies the format of the <i>varPath</i> parameter.


### -param lFormat [in]

Contains one of the <a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor returned in the <i>pVariant</i> parameter. The following list identifies the possible values for this parameter and the format that is supplied in the <i>pVariant</i> parameter.



#### ADS_SD_FORMAT_IID

<i>pVariant</i> receives a <b>VT_DISPATCH</b> that can be queried for the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface.



#### ADS_SD_FORMAT_RAW

<i>pVariant</i> receives a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.



#### ADS_SD_FORMAT_HEXSTRING

<i>pVariant</i> receives a <b>VT_BSTR</b> that contains the raw security descriptor in hex encode string format.


### -param pVariant [out]

Pointer to a <b>VARIANT</b> that receives the returned security descriptor. The format of the retrieved security descriptor is specified by the <i>lFormat</i> parameter.


## -returns



Returns <b>S_OK</b> if successful or a COM or Win32 error code otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f0f5c1fb-14fa-4d84-aa82-0d5e24ec5c2b">SetSecurityDescriptor</a>
 

 


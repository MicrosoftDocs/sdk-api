---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

<i>pVariant</i> receives a <b>VT_I1</b> | <b>VT_ARRAY</b> that contains the security descriptor in raw data format. This is in the format of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure.



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



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f0f5c1fb-14fa-4d84-aa82-0d5e24ec5c2b">SetSecurityDescriptor</a>
 

 


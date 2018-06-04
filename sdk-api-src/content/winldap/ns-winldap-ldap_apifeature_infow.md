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

# ldap_apifeature_infoW structure


## -description


The <b>LDAPAPIFeatureInfo</b> structure retrieves data about any supported LDAP API extensions.


## -struct-fields




### -field ldapaif_info_version

The version of this structure, which must be set to <b>LDAP_FEATURE_INFO_VERSION</b> before the call to <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a> is performed.


### -field ldapaif_name

A pointer to a null-terminated string that contains the name of the desired API extension.  This value is set before the call to <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a> is performed, and should match one of the strings returned in the <b>ldapai_extensions</b> member of <a href="https://msdn.microsoft.com/9175224c-82f0-4f22-9975-b1d7a332c3df">LDAPAPIInfo</a> set  from a previous call to <b>ldap_get_option</b>.


### -field ldapaif_version

The vendor API extension version number.  This implementation returns an integer value in the format of MMnnn, where MM is the major version number * 1000, and nnn is the minor version number.  For example, version 1.001 would be returned as the number 1001.


## -remarks



A pointer to this structure is passed, along with the <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_FEATURE_API_INFO</a> session option and the name of the desired API extension, to <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>, to retrieve detailed data about the LDAP API extension.




## -see-also




<a href="https://msdn.microsoft.com/9175224c-82f0-4f22-9975-b1d7a332c3df">LDAPAPIInfo</a>



<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>



<a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>
 

 


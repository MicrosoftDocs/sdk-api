---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0088_0001
title: "__MIDL___MIDL_itf_ads_0001_0088_0001"
author: windows-sdk-content
description: The ADS_PATHTYPE_ENUM enumeration specifies the type of object on which the IADsSecurityUtility interface is going to add or modify a security descriptor.
old-location: adsi\ads_pathtype_enum.htm
old-project: ADSI
ms.assetid: 3ae0ec98-9184-4ab3-b859-39c0d677eb0d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADS_PATHTYPE_ENUM, ADS_PATHTYPE_ENUM enumeration [ADSI], ADS_PATH_FILE, ADS_PATH_FILESHARE, ADS_PATH_REGISTRY, __MIDL___MIDL_itf_ads_0001_0088_0001, _ds_ads_pathtype_enum, adsi.ads__pathtype__enum, adsi.ads_pathtype_enum, iads/ADS_PATHTYPE_ENUM, iads/ADS_PATH_FILE, iads/ADS_PATH_FILESHARE, iads/ADS_PATH_REGISTRY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADS_PATHTYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_PATHTYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_ads_0001_0088_0001 enumeration


## -description


The <b>ADS_PATHTYPE_ENUM</b> enumeration specifies the type of object on which the <a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a> interface is going to add or modify a security descriptor.


## -enum-fields




### -field ADS_PATH_FILE

Indicates that the security descriptor will be retrieved or set on a file object.


### -field ADS_PATH_FILESHARE

Indicates that the security descriptor will be retrieved or set on a file share object.


### -field ADS_PATH_REGISTRY

Indicates that the security descriptor will be retrieved or set on a registry key object.


## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>



<a href="https://msdn.microsoft.com/7233a82f-fc38-4718-b674-4e6a00666184">Security Descriptors on Files and Registry Keys</a>
 

 


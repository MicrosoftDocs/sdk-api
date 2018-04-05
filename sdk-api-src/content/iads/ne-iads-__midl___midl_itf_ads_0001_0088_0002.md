---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0088_0002
title: "__MIDL___MIDL_itf_ads_0001_0088_0002"
author: windows-driver-content
description: The ADS_SD_FORMAT_ENUM enumeration specifies the format that the security descriptor of an object will be converted to by the IADsSecurityUtility interface.
old-location: adsi\ads_sd_format_enum.htm
old-project: ADSI
ms.assetid: 503247b6-3119-4514-9831-c8f0ef50c0fa
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ADS_SD_FORMAT_ENUM, ADS_SD_FORMAT_ENUM enumeration [ADSI], ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, __MIDL___MIDL_itf_ads_0001_0088_0002, _ds_ads_sd_format_enum, adsi.ads__sd__format__enum, adsi.ads_sd_format_enum, iads/ADS_SD_FORMAT_ENUM, iads/ADS_SD_FORMAT_HEXSTRING, iads/ADS_SD_FORMAT_IID, iads/ADS_SD_FORMAT_RAW
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_SD_FORMAT_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_ads_0001_0088_0002 enumeration


## -description


The <b>ADS_SD_FORMAT_ENUM</b> enumeration specifies the format that the security descriptor of an object will be converted to by the <a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a> interface.


## -enum-fields




### -field ADS_SD_FORMAT_IID

Indicates that the security descriptor is to be converted to the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface format. If <b>ADS_SD_FORMAT_IID</b> is used as the input format when setting the security descriptor, the variant passed in is expected to be a VT_DISPATCH, where the dispatch pointer supports the <b>IADsSecurityDescriptor</b> interface.


### -field ADS_SD_FORMAT_RAW

Indicates that the security descriptor is to be converted to the binary format.


### -field ADS_SD_FORMAT_HEXSTRING

Indicates that the security descriptor is to be converted to the hex encoded string format.


## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>



<a href="https://msdn.microsoft.com/7233a82f-fc38-4718-b674-4e6a00666184">Security Descriptors on Files and Registry Keys</a>
 

 


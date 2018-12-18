---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0016
title: ADS_DN_WITH_STRING
author: windows-sdk-content
description: Used with the ADSVALUE structure to contain a distinguished name attribute value that also contains string data.
old-location: adsi\ads_dn_with_string.htm
tech.root: adsi
ms.assetid: 715354fe-1e62-4fbd-a5ba-0d7a56b83390
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PADS_DN_WITH_STRING, ADS_DN_WITH_STRING, ADS_DN_WITH_STRING structure [ADSI], _ds_ads_dn_with_string, adsi.ads__dn__with__string, adsi.ads_dn_with_string, iads/ADS_DN_WITH_STRING"
ms.topic: struct
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_DN_WITH_STRING
product: Windows
targetos: Windows
req.typenames: ADS_DN_WITH_STRING, *PADS_DN_WITH_STRING
req.redist: 
---

# ADS_DN_WITH_STRING structure


## -description


The <b>ADS_DN_WITH_STRING</b> structure is used with the <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structure to contain a distinguished name attribute value that also contains string data.


## -struct-fields




### -field pszStringValue

Pointer to a null-terminated Unicode string that contains the string value of the attribute.


### -field pszDNString

Pointer to a null-terminated Unicode string that contains the distinguished name.


## -remarks



When extending the active directory schema to add <b>ADS_DN_WITH_STRING</b>, you must also specify the otherWellKnownGuid attribute definition. Add the following to the ldf file attribute definition: omObjectClass:: KoZIhvcUAQEBDA==




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>



<a href="ad.win2k_s_object_dn_string">Object(DN-String)</a>
 

 


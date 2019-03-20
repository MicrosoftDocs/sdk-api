---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0004
title: ADS_PROV_SPECIFIC (iads.h)
author: windows-sdk-content
description: The ADS_PROV_SPECIFIC structure contains provider-specific data represented as a binary large object (BLOB).
old-location: adsi\ads_prov_specific.htm
tech.root: adsi
ms.assetid: 45927280-7fb5-49a6-8ecd-f0a6931bed6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PADS_PROV_SPECIFIC, ADS_PROV_SPECIFIC, ADS_PROV_SPECIFIC structure [ADSI], PADS_PROV_SPECIFIC, PADS_PROV_SPECIFIC structure pointer [ADSI], _ds_ads_prov_specific, adsi.ads__prov__specific, adsi.ads_prov_specific, iads/ADS_PROV_SPECIFIC, iads/PADS_PROV_SPECIFIC"
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
 - ADS_PROV_SPECIFIC
product: Windows
targetos: Windows
req.typenames: ADS_PROV_SPECIFIC, *PADS_PROV_SPECIFIC
req.redist: 
---

# ADS_PROV_SPECIFIC structure


## -description


The <b>ADS_PROV_SPECIFIC</b> structure contains provider-specific data represented as a binary large object (BLOB).


## -struct-fields




### -field dwLength

The size of the character array.


### -field lpValue

A pointer to an array of bytes.


## -remarks



The <b>ADS_PROV_SPECIFIC</b> structure is one of the data types used as a member of the  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structure definition. The data is represented as a BLOB here, although the actual data can be packed in any format, such as a C structure. The provider writer must publish the specific data format under the BLOB.

ADSI may also return attributes as <b>ADS_PROV_SPECIFIC</b> if unable to determine the correct attribute syntax type as would occur if, for example, the schema was unavailable.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>
 

 


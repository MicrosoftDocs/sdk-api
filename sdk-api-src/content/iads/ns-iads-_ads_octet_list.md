---
UID: NS:iads._ADS_OCTET_LIST
title: "_ADS_OCTET_LIST"
author: windows-driver-content
description: The ADS_OCTET_LIST structure is an ADSI representation of an ordered sequence of single-byte strings.
old-location: adsi\ads_octet_list.htm
old-project: ADSI
ms.assetid: 9a6a6ba8-afe1-44d3-a9a8-dab1c5f4265e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PADS_OCTET_LIST, ADS_OCTET_LIST, ADS_OCTET_LIST structure [ADSI], PADS_OCTET_LIST, PADS_OCTET_LIST structure pointer [ADSI], _ADS_OCTET_LIST, _ds_ads_octet_list, adsi.ads__octet__list, adsi.ads_octet_list, iads/ADS_OCTET_LIST, iads/PADS_OCTET_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ADS_OCTET_LIST, *PADS_OCTET_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_OCTET_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ADS_OCTET_LIST structure


## -description


The <b>ADS_OCTET_LIST</b> structure is an ADSI representation of an ordered sequence of single-byte strings.


## -struct-fields




### -field Next

Pointer to the next <b>ADS_OCTET_LIST</b> entry in the list.


### -field Length

Contains the length, in bytes, of the list.


### -field Data

Pointer to an array of BYTEs that contains the list. The <b>Length</b> member of this structure contains the number of BYTEs in this array.


## -remarks



For more information, see Novell NetWare Directory Services Schema Specification, version 1.1.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 


---
UID: NS:iads._ADS_CASEIGNORE_LIST
title: "_ADS_CASEIGNORE_LIST"
author: windows-sdk-content
description: The ADS_CASEIGNORE_LIST structure is an ADSI representation of the Case Ignore List attribute syntax.
old-location: adsi\ads_caseignore_list.htm
old-project: ADSI
ms.assetid: 448c4541-7478-44f3-9be3-f1200f83978a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PADS_CASEIGNORE_LIST, ADS_CASEIGNORE_LIST, ADS_CASEIGNORE_LIST structure [ADSI], PADS_CASEIGNORE_LIST, PADS_CASEIGNORE_LIST structure pointer [ADSI], _ADS_CASEIGNORE_LIST, _ds_ads_caseignore_list, adsi.ads__caseignore__list, adsi.ads_caseignore_list, iads/ADS_CASEIGNORE_LIST, iads/PADS_CASEIGNORE_LIST"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ADS_CASEIGNORE_LIST, *PADS_CASEIGNORE_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_CASEIGNORE_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ADS_CASEIGNORE_LIST structure


## -description


The <b>ADS_CASEIGNORE_LIST</b> structure is an ADSI representation of the <b>Case Ignore List</b> attribute syntax.


## -struct-fields




### -field Next

Pointer to the next <b>ADS_CASEIGNORE_LIST</b> in the list of case-insensitive strings.


### -field String

The null-terminated Unicode string value of the current entry of the list.


## -remarks



A <b>Case Ignore List</b> attribute represents an ordered sequence of case insensitive strings.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 


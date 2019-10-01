---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0005
title: ADS_PATH (iads.h)
author: windows-sdk-content
description: The ADS_PATH structure is an ADSI representation of the Path attribute syntax.
old-location: adsi\ads_path.htm
tech.root: adsi
ms.assetid: b8393a81-3e2a-4e59-a6be-def779efbe82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PADS_PATH, ADS_PATH, ADS_PATH structure [ADSI], PADS_PATH, PADS_PATH structure pointer [ADSI], _ds_ads_path, adsi.ads__path, adsi.ads_path, iads/ADS_PATH, iads/PADS_PATH"
ms.topic: struct
f1_keywords: 
 - "iads/ADS_PATH"
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
 - ADS_PATH
targetos: Windows
req.typenames: ADS_PATH, *PADS_PATH
req.redist: 
ms.custom: 19H1
---

# ADS_PATH structure


## -description


The <b>ADS_PATH</b> structure is an ADSI representation of the <b>Path</b> attribute syntax.


## -struct-fields




### -field Type

Type of file in the file system.


### -field VolumeName

The null-terminated Unicode string that contains the name of an existing volume in the file system.


### -field Path

The null-terminated Unicode string that contains the path of a directory in the file system.


## -remarks



The <b>Path</b> attribute in represents a file system path.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>
 

 


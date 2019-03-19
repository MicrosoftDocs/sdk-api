---
UID: NS:ndattrib.tagOCTET_STRING
title: OCTET_STRING (ndattrib.h)
author: windows-sdk-content
description: The OCTET_STRING structure contains a pointer to a string of byte data.
old-location: ndf\octet_string.htm
tech.root: NDF
ms.assetid: 6133c69d-45ad-4080-b3e1-f42cbdc6cdf7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*POCTET_STRING, OCTET_STRING, OCTET_STRING structure [NDF], OCTET_STRING,*POCTET_STRING, OCTET_STRING,*POCTET_STRING structure [NDF], ndattrib/OCTET_STRING, ndf.octet_string"
ms.topic: struct
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndattrib.idl
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
 - ndattrib.h
api_name:
 - OCTET_STRING, *POCTET_STRING
product: Windows
targetos: Windows
req.typenames: OCTET_STRING, *POCTET_STRING
req.redist: 
---

# OCTET_STRING structure


## -description


The <b>OCTET_STRING</b> structure contains a pointer to a string of byte data.


## -struct-fields




### -field dwLength

Type: <b>DWORD</b>

The length of the data.


### -field lpValue

Type: <b>[size_is(dwLength)]BYTE*</b>

A pointer to the byte array containing the data.


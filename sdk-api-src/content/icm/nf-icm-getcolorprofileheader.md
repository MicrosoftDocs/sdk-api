---
UID: NF:icm.GetColorProfileHeader
title: GetColorProfileHeader
description: Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile. Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned. Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - mscms.dll
api_name:
 - GetColorProfileHeader
f1_keywords:
 - GetColorProfileHeader
 - icm/GetColorProfileHeader
dev_langs:
 - c++
---

## -description

Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile. Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned. Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.

## -parameters

### -param hProfile

Specifies a handle to the color profile in question.

### -param pHeader

Points to a variable in which the ICC header structure is to be placed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. This function will fail is an invalid ICC or WCS XML profile is referenced in the hProfile parameter. For extended error information, call **GetLastError**.

## -remarks

To determine whether the header is derived from an ICC or DMP profile handle, check the header signature (header bytes 36-39). If the signature is "acsp" (big endian) then an ICC profile was used. If the signature is "cdmp" (big-endian) then a DMP was used.

The distinguishing features that identify a header as having been "synthesized" for a WCS DMP are:

pIcmProfileHeader-&gt;phSignature = 'pmdc' (little endian = big endian 'cdmp')

pIcmProfileHeader-&gt;phCMMType = '1scw' (little endian = big endian 'wcs1').

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [PROFILEHEADER](/windows/win32/api/icm/ns-icm-profileheader)

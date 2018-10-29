---
UID: NS:dvdmedia._AM_DVDCOPY_BUSKEY
title: "_AM_DVDCOPY_BUSKEY"
author: windows-sdk-content
description: Identifies the DVD bus key.
old-location: dshow\am_dvdcopy_buskey.htm
tech.root: DirectShow
ms.assetid: 9f55dcc1-cb59-40ce-82d0-7f2066cb9d03
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PAM_DVDCOPY_BUSKEY, AM_DVDCOPY_BUSKEY, AM_DVDCOPY_BUSKEY structure [DirectShow], PAM_DVDCOPY_BUSKEY, PAM_DVDCOPY_BUSKEY structure pointer [DirectShow], _AM_DVDCOPY_BUSKEY, dshow.am_dvdcopy_buskey, dvdmedia/AM_DVDCOPY_BUSKEY, dvdmedia/PAM_DVDCOPY_BUSKEY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dvdmedia.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DVDCOPY_BUSKEY
product: Windows
targetos: Windows
req.typenames: AM_DVDCOPY_BUSKEY, *PAM_DVDCOPY_BUSKEY
req.redist: 
---

# _AM_DVDCOPY_BUSKEY structure


## -description



Identifies the DVD bus key.




## -struct-fields




### -field BusKey

DVD drive bus key.


### -field Reserved

Reserved.


## -remarks



The AM_PROPERTY_DVDCOPY_DVD_KEY1 and AM_PROPERTY_DVDCOPY_DEC_KEY2 properties use this structure.

A bus key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.




## -see-also




<a href="https://msdn.microsoft.com/da3abefd-8f25-449d-8787-84d2cef928da">DVD Copy Protection Property Set</a>
 

 


---
UID: NS:dvdmedia._AM_DVDCOPY_CHLGKEY
title: "_AM_DVDCOPY_CHLGKEY"
author: windows-sdk-content
description: Identifies the DVD challenge key.
old-location: dshow\am_dvdcopy_chlgkey.htm
old-project: DirectShow
ms.assetid: da129f9c-fe30-42f7-b7ca-dfb352b1810d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: "*PAM_DVDCOPY_CHLGKEY, AM_DVDCOPY_CHLGKEY, AM_DVDCOPY_CHLGKEY structure [DirectShow], PAM_DVDCOPY_CHLGKEY, PAM_DVDCOPY_CHLGKEY structure pointer [DirectShow], _AM_DVDCOPY_CHLGKEY, dshow.am_dvdcopy_chlgkey, dvdmedia/AM_DVDCOPY_CHLGKEY, dvdmedia/PAM_DVDCOPY_CHLGKEY"
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
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_DVDCOPY_CHLGKEY, *PAM_DVDCOPY_CHLGKEY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DVDCOPY_CHLGKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _AM_DVDCOPY_CHLGKEY structure


## -description



Identifies the DVD challenge key.




## -struct-fields




### -field ChlgKey

Challenge key.


### -field Reserved

Reserved.


## -remarks



The AM_PROPERTY_DVDCOPY_CHLG_KEY property uses this structure.

A challenge key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.




## -see-also




<a href="https://msdn.microsoft.com/da3abefd-8f25-449d-8787-84d2cef928da">DVD Copy Protection Property Set</a>
 

 


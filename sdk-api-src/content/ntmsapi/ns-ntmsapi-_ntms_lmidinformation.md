---
UID: NS:ntmsapi._NTMS_LMIDINFORMATION
title: "_NTMS_LMIDINFORMATION"
author: windows-sdk-content
description: The NTMS_LMIDINFORMATION structure defines the properties specific to a logical media object.
old-location: fs\ntms_lmidinformation.htm
tech.root: Rsm
ms.assetid: f1a003af-101a-4f1f-b644-392e5542e8dd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NTMS_LMIDINFORMATION, NTMS_LMIDINFORMATION structure [Files], _NTMS_LMIDINFORMATION, _zaw_ntms_lmidinformation, base.ntms_lmidinformation, fs.ntms_lmidinformation, ntmsapi/NTMS_LMIDINFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Ntmsapi.h
api_name:
 - NTMS_LMIDINFORMATION
product: Windows
targetos: Windows
req.typenames: NTMS_LMIDINFORMATION
req.redist: 
---

# _NTMS_LMIDINFORMATION structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_LMIDINFORMATION</b> structure defines the properties specific to a logical media object.


## -struct-fields




### -field MediaPool

Unique identifier of the media pool that contains the logical media.


### -field dwNumberOfPartitions

Number of sides in the media object.


## -remarks



The 
<b>NTMS_LMIDINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 


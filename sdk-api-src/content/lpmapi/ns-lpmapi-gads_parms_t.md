---
UID: NS:lpmapi.Gads_parms_t
title: Gads_parms_t
author: windows-sdk-content
description: The Gads_parms_t structure stores guaranteed service Adspec parameters.
old-location: qos\gads_parms_t.htm
old-project: qos
ms.assetid: 06492722-948d-407a-b1bf-e1c4f5ea7f89
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: Gads_parms_t, Gads_parms_t structure [QOS], lpmapi/Gads_parms_t, qos.gads_parms_t
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: Gads_parms_t
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - Gads_parms_t
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Gads_parms_t structure


## -description


The 
<b>Gads_parms_t</b> structure stores guaranteed service Adspec parameters.


## -struct-fields




### -field Gads_serv_hdr

General information and length information for the guaranteed service Adspec object (this structure), expressed as an <a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a> structure.


### -field Gads_Ctot_hdr

Parameter header for the guaranteed service Adspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Gads_Ctot

Parameter associated with <b>Gads_Ctot_hdr</b>.


### -field Gads_Dtot_hdr

Parameter header for the guaranteed service Adspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Gads_Dtot

Parameter associated with <b>Gads_Dtot_hdr</b>.


### -field Gads_Csum_hdr

Parameter header for the guaranteed service Adspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Gads_Csum

Parameter associated with <b>Gads_Csum</b>.


### -field Gads_Dsum_hdr

Parameter header for the guaranteed service Adspec, expressed as an <a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a> structure.


### -field Gads_Dsum

Parameter associated with <b>Gads_Dsum</b>.


## -remarks



This object may be followed by override general parameter values.




## -see-also




<a href="https://msdn.microsoft.com/56ca242e-d5e9-4c16-9c8e-70a356375683">IntServParmHdr</a>



<a href="https://msdn.microsoft.com/63e6a944-f16e-4b90-ab77-22e5c8ef3fb2">IntServServiceHdr</a>
 

 


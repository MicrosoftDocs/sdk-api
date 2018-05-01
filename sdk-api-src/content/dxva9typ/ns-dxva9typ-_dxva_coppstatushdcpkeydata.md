---
UID: NS:dxva9typ._DXVA_COPPStatusHDCPKeyData
title: "_DXVA_COPPStatusHDCPKeyData"
author: windows-driver-content
description: Contains the result from an HDCP Key Data query in Certified Output Protection Protocol (COPP). This query returns the device's HDCP key selection vector (KSV).
old-location: dshow\dxva_coppstatushdcpkeydata.htm
old-project: DirectShow
ms.assetid: fd49c50d-6caa-4d2a-83c6-41ff0130160f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DXVA_COPPStatusHDCPKeyData, DXVA_COPPStatusHDCPKeyData structure [DirectShow], DXVA_COPPStatusHDCPKeyDataStructure, _DXVA_COPPStatusHDCPKeyData, dshow.dxva_coppstatushdcpkeydata, dxva9typ/DXVA_COPPStatusHDCPKeyData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
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
req.typenames: DXVA_COPPStatusHDCPKeyData
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva9typ.h
api_name:
-	DXVA_COPPStatusHDCPKeyData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_COPPStatusHDCPKeyData structure


## -description



Contains the result from an HDCP Key Data query in Certified Output Protection Protocol (COPP). This query returns the device's HDCP key selection vector (KSV).




## -struct-fields




### -field rApp

A 128-bit random number that was passed by the application in the <a href="https://msdn.microsoft.com/988e6d54-f241-4cfc-8793-fc42de92ac52">AMCOPPStatusInput</a> structure.


### -field dwFlags

Status flag. See <a href="https://msdn.microsoft.com/9109bb2c-1422-4629-b2df-ac877d3cd86e">COPP_StatusFlags</a>.


### -field dwHDCPFlags

Receives zero or more flags from the <a href="https://msdn.microsoft.com/40ad7f00-9b4f-4c2d-8c6b-05725a072bfc">COPP_StatusHDCPFlags</a> enumeration. If the COPP_HDCPRepeater flag is present, the application should not play the content using this graphics adapter.


### -field BKey

Receives the HDCP key selection vector, B<sub>KSV</sub>, from the HDSCP device attached to the graphics adapter.


### -field Reserved1

Reserved. Must be zero.


### -field Reserved2

Reserved. Must be zero.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 


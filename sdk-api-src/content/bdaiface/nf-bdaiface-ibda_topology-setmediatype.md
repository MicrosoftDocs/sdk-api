---
UID: NF:bdaiface.IBDA_Topology.SetMediaType
title: IBDA_Topology::SetMediaType
author: windows-driver-content
description: The SetMediaType method sets the media type for a pin on a BDA device filter.
old-location: mstv\ibda_topology_setmediatype.htm
old-project: mstv
ms.assetid: 69cedd00-3a32-4fb9-91af-2980c314324f
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IBDA_Topology interface [Microsoft TV Technologies],SetMediaType method, IBDA_Topology.SetMediaType, IBDA_Topology::SetMediaType, IBDA_TopologySetMediaType, SetMediaType, SetMediaType method [Microsoft TV Technologies], SetMediaType method [Microsoft TV Technologies],IBDA_Topology interface, bdaiface/IBDA_Topology::SetMediaType, mstv.ibda_topology_setmediatype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_Topology.SetMediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_Topology::SetMediaType


## -description



The <b>SetMediaType</b> method sets the media type for a pin on a BDA device filter.




## -parameters




### -param ulPinId [in]

The identifier of the pin on which to set the media type.


### -param pMediaType [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that contains the media type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35dfe39e-05b4-4c7b-9358-081429b064f2">IBDA_Topology Interface</a>
 

 


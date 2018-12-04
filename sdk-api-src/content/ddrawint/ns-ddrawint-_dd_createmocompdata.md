---
UID: NS:ddrawint._DD_CREATEMOCOMPDATA
title: "_DD_CREATEMOCOMPDATA"
author: windows-sdk-content
description: The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation.
old-location: display\dd_createmocompdata.htm
tech.root: display
ms.assetid: 53b2aa38-b007-4938-8fdb-c3482735ae36
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*PDD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA structure [Display Devices], _DD_CREATEMOCOMPDATA, ddrawint/DD_CREATEMOCOMPDATA, ddstrcts_776346bf-3538-4965-b747-a017a7c21514.xml, display.dd_createmocompdata"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
 - ddrawint.h
api_name:
 - DD_CREATEMOCOMPDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA"
req.redist: 
---

# _DD_CREATEMOCOMPDATA structure


## -description


The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/41cde03a-f9da-4701-a0df-0dba0c17ba26">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation object.


### -field lpGuid

Points to a GUID that describes the motion compensation process being used.


### -field dwUncompWidth

Specifies the width in pixels of the uncompressed output frame. 


### -field dwUncompHeight

Specifies the height in pixels of the uncompressed output frame. 


### -field ddUncompPixelFormat

Points to a <a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a> structure that contains the format of the uncompressed output frame. 


### -field lpData

Points to an optional data buffer that contains any optional information required by the GUID given in <b>lpGuid</b>. This buffer cannot contain any embedded pointers.


### -field dwDataSize

Indicates the size in bytes of the data buffer contained in <b>lpData</b>. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a>
 

 


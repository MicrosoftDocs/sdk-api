---
UID: NS:ddrawint._DD_GETMOCOMPCOMPBUFFDATA
title: "_DD_GETMOCOMPCOMPBUFFDATA"
author: windows-sdk-content
description: The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information.
old-location: display\dd_getmocompcompbuffdata.htm
tech.root: display
ms.assetid: 5510d430-834c-42ea-a113-c17b1b87ea52
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*PDD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA structure [Display Devices], _DD_GETMOCOMPCOMPBUFFDATA, ddrawint/DD_GETMOCOMPCOMPBUFFDATA, ddstrcts_20d1802e-7979-4336-b730-a161f771c24a.xml, display.dd_getmocompcompbuffdata"
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
 - DD_GETMOCOMPCOMPBUFFDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_GETMOCOMPCOMPBUFFDATA, DD_GETMOCOMPCOMPBUFFDATA"
req.redist: 
---

# _DD_GETMOCOMPCOMPBUFFDATA structure


## -description


The DD_GETMOCOMPCOMPBUFFDATA structure contains the compressed buffer information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpGuid

Points to a GUID for which the compressed buffer information is requested. 


### -field dwWidth

Indicates the width in pixels of the uncompressed output frame.


### -field dwHeight

Indicates the height in pixels of the uncompressed output frame.


### -field ddPixelFormat

Points to a <a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.


### -field dwNumTypesCompBuffs

Indicates how many different types of surfaces the driver requires to perform motion compensation using the requested GUID. 


### -field lpCompBuffInfo

Points to a <a href="https://msdn.microsoft.com/73dad759-499f-45b2-9345-4577deb01492">DDCOMPBUFFERINFO</a> structure that contains the driver-supplied information for each type of required surface. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a>
 

 


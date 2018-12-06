---
UID: NS:ddrawint._DD_SYNCVIDEOPORTDATA
title: "_DD_SYNCVIDEOPORTDATA"
author: windows-sdk-content
description: The DD_SYNCVIDEOPORTDATA structure contains the video port extensions (VPE) object information.
old-location: display\dd_syncvideoportdata.htm
tech.root: display
ms.assetid: babe7d53-f278-44f7-9346-b4661b603123
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDD_SYNCVIDEOPORTDATA, DD_SYNCVIDEOPORTDATA, DD_SYNCVIDEOPORTDATA structure [Display Devices], _DD_SYNCVIDEOPORTDATA, ddrawint/DD_SYNCVIDEOPORTDATA, ddstrcts_7a531397-4c11-491f-8cec-8db6b9dfdd0d.xml, display.dd_syncvideoportdata"
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
 - DD_SYNCVIDEOPORTDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_SYNCVIDEOPORTDATA, DD_SYNCVIDEOPORTDATA"
req.redist: 
---

# _DD_SYNCVIDEOPORTDATA structure


## -description


The DD_SYNCVIDEOPORTDATA structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/c497d1ef-0eb1-465f-978c-60cf5606de93">DD_VIDEOPORT_LOCAL</a> structure that describes the hardware video port with which to sync. 


### -field dwOriginOffset

Contains the byte offset from the top left corner of the surface to the top left corner of where the VPE object writes its data. This value is only used by the video miniport driver. This member must contain data that is filled in by the driver. 


### -field dwHeight

Contains the height in pixels of the VPE object data. By default, this is twice the field height when interleaved, but the driver can change this if it needs to. This value is used only by the video miniport driver. This member can be modified by the driver, but does not need to be. 


### -field dwVBIHeight

Contains the number of lines in the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> region. This value is used only by the video miniport driver. This member can be modified by the driver, but does not need to be. 


### -field dwDriverReserved1

Is reserved for use by the display driver.


### -field dwDriverReserved2

Reserved for use by the display driver.


### -field dwDriverReserved3

Reserved for use by the display driver.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/3726a505-c3cf-4784-886e-2f4524fb0c5b">DdSyncVideoPortData</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/3726a505-c3cf-4784-886e-2f4524fb0c5b">DdSyncVideoPortData</a>
 

 


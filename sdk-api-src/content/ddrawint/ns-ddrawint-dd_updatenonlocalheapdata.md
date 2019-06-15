---
UID: NS:ddrawint._DD_UPDATENONLOCALHEAPDATA
title: DD_UPDATENONLOCALHEAPDATA (ddrawint.h)
author: windows-sdk-content
description: The DD_UPDATENONLOCALHEAPDATA structure contains the required heap information.
old-location: display\dd_updatenonlocalheapdata.htm
tech.root: display
ms.assetid: ef16df6f-dbc6-40ee-9c86-be9c3d132b28
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA structure [Display Devices], ddrawint/DD_UPDATENONLOCALHEAPDATA, ddstrcts_e53429c7-6fc5-4528-ab0e-c9768fdf75ae.xml, display.dd_updatenonlocalheapdata"
ms.topic: struct
f1_keywords: ["ddrawint/DD_UPDATENONLOCALHEAPDATA"]
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
 - DD_UPDATENONLOCALHEAPDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA"
req.redist: 
ms.custom: 19H1
---

# DD_UPDATENONLOCALHEAPDATA structure


## -description


The DD_UPDATENONLOCALHEAPDATA structure contains the required heap information.


## -struct-fields




### -field lpDD

Points to the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device. 


### -field dwHeap

Indicates the ordinal number of the heap for which data is being requested.


### -field fpGARTLin

Points to the linear graphic address remapping table (GART) address of the start of the heap. 


### -field fpGARTDev

Points to the physical GART address of the start of the heap. 


### -field ulPolicyMaxBytes

Indicates the maximum amount of AGP memory to use. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> callback for a GUID_UpdateNonLocalHeap query. A return code of DD_OK indicates success. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.


### -field UpdateNonLocalHeap

Unused on Microsoft Windows 2000 and later versions of the operating system.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>
 

 


---
UID: NS:dmemmgr._DD_GETHEAPALIGNMENTDATA
title: DD_GETHEAPALIGNMENTDATA (dmemmgr.h)
author: windows-sdk-content
description: The DD_GETHEAPALIGNMENTDATA structure contains data on required alignments from a particular heap.
old-location: display\dd_getheapalignmentdata.htm
tech.root: display
ms.assetid: 5bdc13e3-396d-45f6-8c90-a831bbb23628
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_GETHEAPALIGNMENTDATA, DD_GETHEAPALIGNMENTDATA, DD_GETHEAPALIGNMENTDATA structure [Display Devices], PDD_GETHEAPALIGNMENTDATA, PDD_GETHEAPALIGNMENTDATA structure pointer [Display Devices], ddstrcts_f3e28642-cebe-4512-9ef4-20cc707a4459.xml, display.dd_getheapalignmentdata, dmemmgr/DD_GETHEAPALIGNMENTDATA, dmemmgr/PDD_GETHEAPALIGNMENTDATA"
ms.topic: struct
f1_keywords: 
 - "dmemmgr/DD_GETHEAPALIGNMENTDATA"
req.header: dmemmgr.h
req.include-header: Dmemmgr.h
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
 - dmemmgr.h
api_name:
 - DD_GETHEAPALIGNMENTDATA
product: Windows
targetos: Windows
req.typenames: DD_GETHEAPALIGNMENTDATA, *PDD_GETHEAPALIGNMENTDATA
req.redist: 
ms.custom: 19H1
---

# DD_GETHEAPALIGNMENTDATA structure


## -description


The DD_GETHEAPALIGNMENTDATA structure contains data on required alignments from a particular heap.


## -struct-fields




### -field dwInstance

Indicates the driver context as returned from the driver initialization routine and stored in the <b>dhpDev</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure. 


### -field dwHeap

Specifies the heap index passed by Microsoft DirectDraw. See the Remarks section for more information.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> callback for a GUID_GetHeapAlignment query. A return code of DD_OK indicates success. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.


### -field GetHeapAlignment

Unused on Microsoft Windows 2000 and later versions of the operating system.


### -field Alignment

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/ns-dmemmgr-_heapalignment">HEAPALIGNMENT</a> structure filled in by the driver.


## -remarks



The <b>dwHeap</b> member is the ordinal number of the heap for which alignment data is being requested. In other words, it is the index into the array of <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_videomemory">VIDEOMEMORY</a> structures pointed to by the <i>pvmList</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a> driver function. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/ns-dmemmgr-_heapalignment">HEAPALIGNMENT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-_videomemory">VIDEOMEMORY</a>
 

 


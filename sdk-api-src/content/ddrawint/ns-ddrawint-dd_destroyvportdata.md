---
UID: NS:ddrawint._DD_DESTROYVPORTDATA
title: DD_DESTROYVPORTDATA
author: windows-sdk-content
description: The DD_DESTROYVPORTDATA structure contains the information necessary for the driver to clean up.
old-location: display\dd_destroyvportdata.htm
tech.root: display
ms.assetid: b9e29c23-bb1a-47e8-a605-2863c4cda2af
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA structure [Display Devices], ddrawint/DD_DESTROYVPORTDATA, ddstrcts_bb54464c-6b2f-4c90-99a9-439938562898.xml, display.dd_destroyvportdata"
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
 - DD_DESTROYVPORTDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_DESTROYVPORTDATA, DD_DESTROYVPORTDATA"
req.redist: 
---

# DD_DESTROYVPORTDATA structure


## -description


The DD_DESTROYVPORTDATA structure contains the information necessary for the driver to clean up.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only. 


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/c497d1ef-0eb1-465f-978c-60cf5606de93">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/0426eeaa-4d9a-4e5e-8550-2f7adbb26685">DdVideoPortDestroy</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field DestroyVideoPort

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/0426eeaa-4d9a-4e5e-8550-2f7adbb26685">DdVideoPortDestroy</a>
 

 


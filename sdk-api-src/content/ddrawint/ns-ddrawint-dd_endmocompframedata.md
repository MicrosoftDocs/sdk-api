---
UID: NS:ddrawint._DD_ENDMOCOMPFRAMEDATA
title: DD_ENDMOCOMPFRAMEDATA (ddrawint.h)
description: The DD_ENDMOCOMPFRAMEDATA structure contains information required to complete a decoded frame.helpviewer_keywords: ["*PDD_ENDMOCOMPFRAMEDATA","DD_ENDMOCOMPFRAMEDATA","DD_ENDMOCOMPFRAMEDATA structure [Display Devices]","ddrawint/DD_ENDMOCOMPFRAMEDATA","ddstrcts_4c526986-eaf4-40ea-890c-e90295ac9ee6.xml","display.dd_endmocompframedata"]
old-location: display\dd_endmocompframedata.htm
tech.root: display
ms.assetid: 4e604940-1c0f-43be-bac7-9936df0c4044
ms.date: 12/05/2018
ms.keywords: '*PDD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA structure [Display Devices], ddrawint/DD_ENDMOCOMPFRAMEDATA, ddstrcts_4c526986-eaf4-40ea-890c-e90295ac9ee6.xml, display.dd_endmocompframedata'
f1_keywords:
- ddrawint/DD_ENDMOCOMPFRAMEDATA
dev_langs:
- c++
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
- DD_ENDMOCOMPFRAMEDATA
targetos: Windows
req.typenames: '*PDD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA'
req.redist: 
ms.custom: 19H1
---

# DD_ENDMOCOMPFRAMEDATA structure


## -description


The DD_ENDMOCOMPFRAMEDATA structure contains information required to complete a decoded frame. 


## -struct-fields




### -field lpDD

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncomp_local">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field lpInputData

Points to an optional buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.


### -field dwInputDataSize

Indicates the size in bytes of data in <b>lpInputData</b>. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a>
 

 


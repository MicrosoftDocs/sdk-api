---
UID: NS:ddrawint._DD_CANCREATEVPORTDATA
title: "_DD_CANCREATEVPORTDATA"
author: windows-sdk-content
description: The DD_CANCREATEVPORTDATA structure contains the information required for the driver to determine whether a video port extensions (VPE) object can be created.
old-location: display\dd_cancreatevportdata.htm
tech.root: display
ms.assetid: 60116f1d-fca2-4282-95a9-2af8da113a20
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PDD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA structure [Display Devices], _DD_CANCREATEVPORTDATA, ddrawint/DD_CANCREATEVPORTDATA, ddstrcts_72b44069-d635-4675-b632-d0d077aa96e8.xml, display.dd_cancreatevportdata"
ms.prod: windows
ms.technology: windows-sdk
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
 - DD_CANCREATEVPORTDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_CANCREATEVPORTDATA, DD_CANCREATEVPORTDATA"
req.redist: 
---

# _DD_CANCREATEVPORTDATA structure


## -description


The DD_CANCREATEVPORTDATA structure contains the information required for the driver to determine whether a <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object can be created.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpDDVideoPortDesc

Points to a <a href="https://msdn.microsoft.com/efd5907c-ed75-40be-b568-7c305310f79b">DDVIDEOPORTDESC</a> structure that contains a description of the VPE object being requested.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/742c7af2-0611-4cca-b18c-e14b18068d7e">DdVideoPortCanCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field CanCreateVideoPort

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/742c7af2-0611-4cca-b18c-e14b18068d7e">DdVideoPortCanCreate</a>
 

 


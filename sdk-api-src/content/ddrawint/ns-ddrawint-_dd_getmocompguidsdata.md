---
UID: NS:ddrawint._DD_GETMOCOMPGUIDSDATA
title: "_DD_GETMOCOMPGUIDSDATA"
author: windows-sdk-content
description: The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information.
old-location: display\dd_getmocompguidsdata.htm
old-project: display
ms.assetid: d1507771-c2bc-4d10-a49e-57a3b60ac604
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*PDD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA structure [Display Devices], _DD_GETMOCOMPGUIDSDATA, ddrawint/DD_GETMOCOMPGUIDSDATA, ddstrcts_fb041d18-05e9-4ef4-bb69-6dedf60bec78.xml, display.dd_getmocompguidsdata"
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
tech.root: 
req.typenames: "*PDD_GETMOCOMPGUIDSDATA, DD_GETMOCOMPGUIDSDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETMOCOMPGUIDSDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_GETMOCOMPGUIDSDATA structure


## -description


The DD_GETMOCOMPGUIDSDATA structure contains the motion compensation GUID information. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field dwNumGuids

Indicates the number of motion compensation GUIDs in <b>lpGuids</b>. 


### -field lpGuids

Points to a list of GUIDs that describe the motion compensation processes being used. If <b>lpGuids</b> is <b>NULL</b>, the driver should set <b>dwNumGuids</b> to the number of GUIDs that it supports. Otherwise, it should fill <b>lpGuids</b> with the GUIDs that it supports and set the number in <b>dwNumGuids</b>.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a>
 

 


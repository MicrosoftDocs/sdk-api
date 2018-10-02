---
UID: NS:ddrawint._DD_UPDATENONLOCALHEAPDATA
title: "_DD_UPDATENONLOCALHEAPDATA"
author: windows-sdk-content
description: The DD_UPDATENONLOCALHEAPDATA structure contains the required heap information.
old-location: display\dd_updatenonlocalheapdata.htm
tech.root: Display
ms.assetid: ef16df6f-dbc6-40ee-9c86-be9c3d132b28
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA structure [Display Devices], _DD_UPDATENONLOCALHEAPDATA, ddrawint/DD_UPDATENONLOCALHEAPDATA, ddstrcts_e53429c7-6fc5-4528-ab0e-c9768fdf75ae.xml, display.dd_updatenonlocalheapdata"
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
 - DD_UPDATENONLOCALHEAPDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_UPDATENONLOCALHEAPDATA, DD_UPDATENONLOCALHEAPDATA"
req.redist: 
---

# _DD_UPDATENONLOCALHEAPDATA structure


## -description


The DD_UPDATENONLOCALHEAPDATA structure contains the required heap information.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device. 


### -field dwHeap

Indicates the ordinal number of the heap for which data is being requested.


### -field fpGARTLin

Points to the linear graphic address remapping table (GART) address of the start of the heap. 


### -field fpGARTDev

Points to the physical GART address of the start of the heap. 


### -field ulPolicyMaxBytes

Indicates the maximum amount of AGP memory to use. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> callback for a GUID_UpdateNonLocalHeap query. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field UpdateNonLocalHeap

Unused on Microsoft Windows 2000 and later versions of the operating system.


## -see-also




<a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 


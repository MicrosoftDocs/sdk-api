---
UID: NS:authif._RADIUS_EXTENSION_CONTROL_BLOCK
title: "_RADIUS_EXTENSION_CONTROL_BLOCK"
author: windows-driver-content
description: The RADIUS_EXTENSION_CONTROL_BLOCK structure provides information about the current RADIUS request. It also provides functions for obtaining the attributes associated with the request, and for setting the disposition of the request.
old-location: nps\IAS_radius_extension_control_block.htm
old-project: Nps
ms.assetid: 13ff0645-d3f8-4220-a5bc-11bb515bca95
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PRADIUS_EXTENSION_CONTROL_BLOCK, PRADIUS_EXTENSION_CONTROL_BLOCK, PRADIUS_EXTENSION_CONTROL_BLOCK structure pointer [Network Policy Server], RADIUS_EXTENSION_CONTROL_BLOCK, RADIUS_EXTENSION_CONTROL_BLOCK structure [Network Policy Server], _RADIUS_EXTENSION_CONTROL_BLOCK, _ias_radius_extension_control_block, authif/PRADIUS_EXTENSION_CONTROL_BLOCK, authif/RADIUS_EXTENSION_CONTROL_BLOCK, ias.radius_extension_control_block, nps.IAS_radius_extension_control_block"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RADIUS_EXTENSION_CONTROL_BLOCK, *PRADIUS_EXTENSION_CONTROL_BLOCK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AuthIf.h
api_name:
-	RADIUS_EXTENSION_CONTROL_BLOCK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _RADIUS_EXTENSION_CONTROL_BLOCK structure


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_EXTENSION_CONTROL_BLOCK</b> structure provides information about the current RADIUS request. It also provides functions for obtaining the attributes associated with the request, and for setting the disposition of the request.


## -struct-fields




### -field cbSize

Specifies the size of the structure.


### -field dwVersion

Specifies the version of the structure.


### -field repPoint

Specifies a value of type 
<a href="https://msdn.microsoft.com/0e7f4d48-01b5-45a8-bf72-27b557ae8da7">RADIUS_EXTENSION_POINT</a> that indicates at what point in the request process 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> was called.


### -field rcRequestType

Specifies a value of type 
<a href="https://msdn.microsoft.com/cb971643-82ca-4302-a961-9d567da04c27">RADIUS_CODE</a> that specifies the type of RADIUS request received by the Internet Authentication Service server.


### -field rcResponseType

Specifies a value of type 
<a href="https://msdn.microsoft.com/cb971643-82ca-4302-a961-9d567da04c27">RADIUS_CODE</a> that indicates the disposition of the RADIUS request.


### -field GetRequest

Pointer to the <a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> function provided by NPS. NPS sets the value of this member.


### -field GetResponse

Pointer to the <a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> function provided by NPS. NPS sets the value of this member.


### -field SetResponseType

Pointer to the <a href="https://msdn.microsoft.com/96e88037-1131-4f7a-9c34-0e86762361db">SetResponseType</a> function provided by NPS. NPS sets the value of this member.


## -remarks



The Extension DLL must not modify this structure. Changes to the array of attributes should be made by calling the functions provided as members of this structure.

NPS passes this structure to the Extension DLL when it calls the Extension DLL's implementation of 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a>.




## -see-also




<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a>



<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a>



<a href="https://msdn.microsoft.com/2eec8b05-c74d-4876-a475-0be7f60014d0">RADIUS_ATTRIBUTE_ARRAY</a>



<a href="https://msdn.microsoft.com/96e88037-1131-4f7a-9c34-0e86762361db">SetResponseType</a>
 

 


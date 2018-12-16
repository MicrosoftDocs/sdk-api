---
UID: NE:authif._RADIUS_EXTENSION_POINT
title: RADIUS_EXTENSION_POINT
author: windows-sdk-content
description: The RADIUS_EXTENSION_POINT enumeration type enumerates the possible points in the RADIUS request process when the RadiusExtensionProcess2 function can be called.
old-location: nps\IAS_radius_extension_point.htm
tech.root: Nps
ms.assetid: 0e7f4d48-01b5-45a8-bf72-27b557ae8da7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RADIUS_EXTENSION_POINT, RADIUS_EXTENSION_POINT enumeration [Network Policy Server], _ias_radius_extension_point, authif/RADIUS_EXTENSION_POINT, authif/repAuthentication, authif/repAuthorization, ias.radius_extension_point, nps.IAS_radius_extension_point, repAuthentication, repAuthorization
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_EXTENSION_POINT
product: Windows
targetos: Windows
req.typenames: RADIUS_EXTENSION_POINT
req.redist: 
---

# RADIUS_EXTENSION_POINT enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_EXTENSION_POINT</b> enumeration type enumerates the possible points in the RADIUS request process when the 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> function can be called.


## -enum-fields




### -field repAuthentication

Indicates that the 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> function is called at the point in the request process where authentication occurs.


### -field repAuthorization

Indicates that the 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> function is called at the point in the request process where authorization occurs.


## -remarks



The <b>repPoint</b> member of the 
<a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a> structure is of type 
<b>RADIUS_EXTENSION_POINT</b>.

See 
<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a> for a diagram that shows the request process.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a>
 

 


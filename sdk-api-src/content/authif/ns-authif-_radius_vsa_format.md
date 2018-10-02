---
UID: NS:authif._RADIUS_VSA_FORMAT
title: "_RADIUS_VSA_FORMAT"
author: windows-sdk-content
description: The RADIUS_VSA_FORMAT structure represents the format of the string portion of a RADIUS vendor-specific attribute.
old-location: nps\IAS_radius_vsa_format.htm
tech.root: Nps
ms.assetid: 6f883a2f-84f1-44f5-8b15-c7e55fae4289
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RADIUS_VSA_FORMAT, RADIUS_VSA_FORMAT structure [Network Policy Server], _RADIUS_VSA_FORMAT, _ias_radius_vsa_format, authif/RADIUS_VSA_FORMAT, ias.radius_vsa_format, nps.IAS_radius_vsa_format
ms.prod: windows
ms.technology: windows-sdk
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
 - RADIUS_VSA_FORMAT
product: Windows
targetos: Windows
req.typenames: RADIUS_VSA_FORMAT
req.redist: 
---

# _RADIUS_VSA_FORMAT structure


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_VSA_FORMAT</b> structure represents the format of the string portion of a RADIUS vendor-specific attribute.


## -struct-fields




### -field VendorId

The SMI Network Management Private Enterprise Code of the vendor for this attribute.


### -field VendorType

Numeric identifier for the attribute assigned by the vendor.


### -field VendorLength

The combined size of the <b>VendorType</b>, <b>VendorLength</b>, <b>AttributeSpecific</b> members.


### -field AttributeSpecific

Array of bytes that contains information for this attribute.


## -remarks



The 
<b>RADIUS_VSA_FORMAT</b> structure is useful for interpreting the <b>lpValue</b> member of a 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structure when the <b>dwAttrType</b> member has a value <b>ratVendorSpecific</b>.

See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for a description of RADIUS vendor-specific attributes. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">RFC 2548</a> for examples of RADIUS vendor-specific attributes used by Microsoft.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/8b13a21c-edbe-4982-8718-a34d62ecc38d">NPS Extensions Structures</a>
 

 


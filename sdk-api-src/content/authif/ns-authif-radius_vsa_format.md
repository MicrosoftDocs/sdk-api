---
UID: NS:authif._RADIUS_VSA_FORMAT
title: RADIUS_VSA_FORMAT (authif.h)
description: The RADIUS_VSA_FORMAT structure represents the format of the string portion of a RADIUS vendor-specific attribute.
helpviewer_keywords: ["RADIUS_VSA_FORMAT","RADIUS_VSA_FORMAT structure [Network Policy Server]","_ias_radius_vsa_format","authif/RADIUS_VSA_FORMAT","ias.radius_vsa_format","nps.IAS_radius_vsa_format"]
old-location: nps\IAS_radius_vsa_format.htm
tech.root: Nps
ms.assetid: 6f883a2f-84f1-44f5-8b15-c7e55fae4289
ms.date: 12/05/2018
ms.keywords: RADIUS_VSA_FORMAT, RADIUS_VSA_FORMAT structure [Network Policy Server], _ias_radius_vsa_format, authif/RADIUS_VSA_FORMAT, ias.radius_vsa_format, nps.IAS_radius_vsa_format
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
targetos: Windows
req.typenames: RADIUS_VSA_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_VSA_FORMAT
 - authif/_RADIUS_VSA_FORMAT
 - RADIUS_VSA_FORMAT
 - authif/RADIUS_VSA_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_VSA_FORMAT
---

# RADIUS_VSA_FORMAT structure


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
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a> structure when the <b>dwAttrType</b> member has a value <b>ratVendorSpecific</b>.

See 
<a href="https://www.ietf.org/rfc/rfc2865.txt">RFC 2865</a> for a description of RADIUS vendor-specific attributes. See 
<a href="https://www.ietf.org/rfc/rfc2548.txt">RFC 2548</a> for examples of RADIUS vendor-specific attributes used by Microsoft.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-structures">NPS Extensions Structures</a>
---
UID: NS:naptypes.tagSoH
title: SoH (naptypes.h)
description: Contains the Statement of Health (SoH) data.
helpviewer_keywords: ["SoH","SoH structure [NAP]","SoHRequest","SoHRequest structure [NAP]","SoHResponse","SoHResponse structure [NAP]","nap.soh_struct","naptypes/SoH","naptypes/SoHRequest","naptypes/SoHResponse"]
old-location: nap\soh_struct.htm
tech.root: NAP
ms.assetid: 6db0303d-ab33-4fb9-90a2-b909b2781ba5
ms.date: 12/05/2018
ms.keywords: SoH, SoH structure [NAP], SoHRequest, SoHRequest structure [NAP], SoHResponse, SoHResponse structure [NAP], nap.soh_struct, naptypes/SoH, naptypes/SoHRequest, naptypes/SoHResponse
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SoH, SoHRequest, SoHResponse
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSoH
 - naptypes/tagSoH
 - SoH
 - naptypes/SoH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - SoH
---

# SoH structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SoH</b> structure contains the Statement of Health (SoH) data.

## -struct-fields

### -field count

The number of attributes contained in the SoH as a number between 0 (zero) and <a href="/windows/desktop/NAP/nap-type-constants">maxSoHAttributeCount</a>.

### -field attributes

An array of <a href="/windows/desktop/api/naptypes/ns-naptypes-sohattribute">SoHAttribute</a> structures that contain the collection of attributes defined by this SoH.

## -remarks

SoH packets are collections of attributes, stored as type-length-value objects (TLVs). The attribute type is specified by <a href="/windows/desktop/NAP/sohattributetype-enum">SoHAttributeType</a>, and the attribute value is specified by <a href="/windows/desktop/NAP/sohattributevalue-union">SoHAttributeValue</a>. The TLVs are ordered
such that certain TLVs (such as the <b>sohAttributeTypeSystemHealthId</b> TLV or the 
<b>sohAttributeTypeHealthClass</b> TLV) separate groups or 
sub-groups of TLVs.

The <a href="/windows/desktop/NAP/sohattributetype-enum">sohAttributeTypeSystemHealthId</a> TLV must be the first TLV in both <b>SoHRequest</b> and <b>SoHResponse</b> packets.
A <b>SoHResponse</b> packet can have at most one <b>sohAttributeTypeIpv4FixupServers</b> or <b>sohAttributeTypeIpv6FixupServers</b> TLV.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>
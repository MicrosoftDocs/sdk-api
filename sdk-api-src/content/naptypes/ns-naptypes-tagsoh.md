---
UID: NS:naptypes.tagSoH
title: tagSoH
author: windows-sdk-content
description: Contains the Statement of Health (SoH) data.
old-location: nap\soh_struct.htm
old-project: nap
ms.assetid: 6db0303d-ab33-4fb9-90a2-b909b2781ba5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: SoH, SoH structure [NAP], SoHRequest, SoHRequest structure [NAP], SoHResponse, SoHResponse structure [NAP], nap.soh_struct, naptypes/SoH, naptypes/SoHRequest, naptypes/SoHResponse, tagSoH
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SoH, SoHRequest, SoHResponse
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - SoH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagSoH structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SoH</b> structure contains the Statement of Health (SoH) data.


## -struct-fields




### -field count

The number of attributes contained in the SoH as a number between 0 (zero) and <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">maxSoHAttributeCount</a>.


### -field attributes

An array of <a href="https://msdn.microsoft.com/cd954277-27e0-47f4-b4c3-f5335925b8fd">SoHAttribute</a> structures that contain the collection of attributes defined by this SoH.


## -remarks



SoH packets are collections of attributes, stored as type-length-value objects (TLVs). The attribute type is specified by <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">SoHAttributeType</a>, and the attribute value is specified by <a href="https://msdn.microsoft.com/53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12">SoHAttributeValue</a>. The TLVs are ordered
such that certain TLVs (such as the <b>sohAttributeTypeSystemHealthId</b> TLV or the 
<b>sohAttributeTypeHealthClass</b> TLV) separate groups or 
sub-groups of TLVs.

The <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">sohAttributeTypeSystemHealthId</a> TLV must be the first TLV in both <b>SoHRequest</b> and <b>SoHResponse</b> packets.
A <b>SoHResponse</b> packet can have at most one <b>sohAttributeTypeIpv4FixupServers</b> or <b>sohAttributeTypeIpv6FixupServers</b> TLV.




## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 


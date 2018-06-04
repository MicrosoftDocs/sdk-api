---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _CERT_LOGOTYPE_INFO structure


## -description


The <b>CERT_LOGOTYPE_INFO</b> structure contains information about logotype data.


## -struct-fields




### -field dwLogotypeInfoChoice

Specifies the type of logotype data. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_DIRECT_INFO_CHOICE"></a><a id="cert_logotype_direct_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_DIRECT_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The logotype data is available directly. The <b>pLogotypeDirectInfo</b> member contains the actual logotype data.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_INDIRECT_INFO_CHOICE"></a><a id="cert_logotype_indirect_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_INDIRECT_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The logotype data is available through a reference. The <b>pLogotypeIndirectInfo</b> member contains a reference to the logotype information.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.pLogotypeDirectInfo

The address of a <a href="https://msdn.microsoft.com/f170dd48-a0f4-45e0-b5b8-a5f446d1a86e">CERT_LOGOTYPE_DATA</a> structure that contains the actual logotype data. This member is only used if the <b>dwLogotypeInfoChoice</b> member contains <b>CERT_LOGOTYPE_DIRECT_INFO_CHOICE</b>.


### -field DUMMYUNIONNAME.pLogotypeIndirectInfo

The address of a <a href="https://msdn.microsoft.com/22e6492e-afc2-4160-ad6c-0b65265eafeb">CERT_LOGOTYPE_REFERENCE</a> structure that contains references to the logotype data. This member is only used if the <b>dwLogotypeInfoChoice</b> member contains <b>CERT_LOGOTYPE_INDIRECT_INFO_CHOICE</b>.


## -see-also




<a href="https://msdn.microsoft.com/5013241b-439e-4aea-9161-699ee69c65c9">CERT_LOGOTYPE_EXT_INFO</a>
 

 


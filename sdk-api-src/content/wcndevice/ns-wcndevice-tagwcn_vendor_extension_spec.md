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

# tagWCN_VENDOR_EXTENSION_SPEC structure


## -description


The <b>WCN_VENDOR_EXTENSION_SPEC</b> structure contains data that defines a vendor extension. 


## -struct-fields




### -field VendorId

Set this value to the SMI Enterprise ID Number of the vendor that defines the vendor extension. For example, the Microsoft ID is '311' (WCN_MICROSOFT_VENDOR_ID).


### -field SubType

The subtype, as defined by the first two bytes of the vendor extension. If the vendor has  not provided the two-byte subtype prefix, use WCN_NO_SUBTYPE. 


### -field Index

Distinguishes between multiple vendor extensions with the same VendorID and SubType. The index begins at zero.


### -field Flags

Applications must specify one of the following flag values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_DISCOVERY_VE"></a><a id="wcn_flag_discovery_ve"></a><dl>
<dt><b>WCN_FLAG_DISCOVERY_VE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The vendor extension was not available  before the session started. The vendor extension is not secure.

</td>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_AUTHENTICATED_VE"></a><a id="wcn_flag_authenticated_ve"></a><dl>
<dt><b>WCN_FLAG_AUTHENTICATED_VE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The vendor extension is authentic. Only devices that pass authentication can read or write authenticated vendor extensions.

</td>
</tr>
<tr>
<td width="40%"><a id="WCN_FLAG_ENCRYPTED_VE"></a><a id="wcn_flag_encrypted_ve"></a><dl>
<dt><b>WCN_FLAG_ENCRYPTED_VE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The vendor extension is authentic and encrypted. In addition to the guarantee of authenticated vendor extensions, vendor extensions are encrypted before transmission.

</td>
</tr>
</table>
 


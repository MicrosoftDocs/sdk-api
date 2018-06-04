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

# _CERT_OTHER_LOGOTYPE_INFO structure


## -description


The <b>CERT_OTHER_LOGOTYPE_INFO</b> structure contains information about logo types that are not predefined.


## -struct-fields




### -field pszObjId

The address of a null-terminated ANSI string that contains the object identifier of the logo type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_LOYALTY_OTHER_LOGOTYPE"></a><a id="szoid_loyalty_other_logotype"></a><a id="SZOID_LOYALTY_OTHER_LOGOTYPE"></a><dl>
<dt><b>szOID_LOYALTY_OTHER_LOGOTYPE</b></dt>
<dt>"1.3.6.1.5.5.7.20.1"</dt>
</dl>
</td>
<td width="60%">
The logo is a loyalty logo.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_BACKGROUND_OTHER_LOGOTYPE"></a><a id="szoid_background_other_logotype"></a><a id="SZOID_BACKGROUND_OTHER_LOGOTYPE"></a><dl>
<dt><b>szOID_BACKGROUND_OTHER_LOGOTYPE</b></dt>
<dt>"1.3.6.1.5.5.7.20.2"</dt>
</dl>
</td>
<td width="60%">
The logo is a background logo.

</td>
</tr>
</table>
 


### -field LogotypeInfo

A <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structure that contains the logo type information.


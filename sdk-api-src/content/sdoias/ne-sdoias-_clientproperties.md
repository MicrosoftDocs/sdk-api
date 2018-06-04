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

# _CLIENTPROPERTIES enumeration


## -description


The values of the 
<b>CLIENTPROPERTIES</b> type enumerate the properties of a RADIUS client. The SDO computer is the RADIUS server.


## -enum-fields




### -field PROPERTY_CLIENT_REQUIRE_SIGNATURE

Specifies whether the RADIUS server checks for a digital signature.

<div class="alert"><b>Note</b>  If client and server use Extensible Authentication Protocol (EAP), then they use digital signatures regardless of this property.</div>
<div> </div>

### -field PROPERTY_CLIENT_UNUSED

This value indicates that the property is not used at this time.


### -field PROPERTY_CLIENT_SHARED_SECRET

The secret shared by both the RADIUS client and RADIUS server.


### -field PROPERTY_CLIENT_NAS_MANUFACTURER

The manufacturer of the Network Access Server (NAS), that is the RADIUS client.


### -field PROPERTY_CLIENT_ADDRESS

The IP address of the RADIUS client.


### -field PROPERTY_CLIENT_QUARANTINE_COMPATIBLE

Used by NPS user interface to indicate whether a RADIUS Client can receive NAP specific quarantine attributes.


### -field PROPERTY_CLIENT_ENABLED

Specifies if the RADIUS Client is enabled. If the RADIUS Client is not enabled, the configuration is present but it is not applied by NPS.


### -field PROPERTY_CLIENT_SECRET_TEMPLATE_GUID




#### - PROPERTY_CLIENT_FILTER_VSAS

This value must be set before a client SDO object can be saved.


## -see-also




<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/adf73b6d-963d-4a06-b958-8301e4fdf292">RADIUSPROPERTIES</a>
 

 


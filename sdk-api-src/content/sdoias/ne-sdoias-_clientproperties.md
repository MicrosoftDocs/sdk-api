---
UID: NE:sdoias._CLIENTPROPERTIES
title: "_CLIENTPROPERTIES"
author: windows-sdk-content
description: The values of the CLIENTPROPERTIES type enumerate the properties of a RADIUS client. The SDO computer is the RADIUS server.
old-location: nps\SDO_clientproperties.htm
tech.root: Nps
ms.assetid: bd37acfb-eb92-40de-945b-ebda95f6ae53
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CLIENTPROPERTIES, CLIENTPROPERTIES enumeration [Network Policy Server], PROPERTY_CLIENT_ADDRESS, PROPERTY_CLIENT_ENABLED, PROPERTY_CLIENT_FILTER_VSAS, PROPERTY_CLIENT_NAS_MANUFACTURER, PROPERTY_CLIENT_QUARANTINE_COMPATIBLE, PROPERTY_CLIENT_REQUIRE_SIGNATURE, PROPERTY_CLIENT_SHARED_SECRET, PROPERTY_CLIENT_UNUSED, _CLIENTPROPERTIES, _sdo_clientproperties, nps.SDO_clientproperties, sdo.clientproperties, sdoias/CLIENTPROPERTIES, sdoias/PROPERTY_CLIENT_ADDRESS, sdoias/PROPERTY_CLIENT_ENABLED, sdoias/PROPERTY_CLIENT_FILTER_VSAS, sdoias/PROPERTY_CLIENT_NAS_MANUFACTURER, sdoias/PROPERTY_CLIENT_QUARANTINE_COMPATIBLE, sdoias/PROPERTY_CLIENT_REQUIRE_SIGNATURE, sdoias/PROPERTY_CLIENT_SHARED_SECRET, sdoias/PROPERTY_CLIENT_UNUSED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
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
 - SdoIas.h
api_name:
 - CLIENTPROPERTIES
product: Windows
targetos: Windows
req.typenames: CLIENTPROPERTIES
req.redist: 
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
 

 


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

# _COPP_ConnectorType enumeration


## -description



Specifies the type of physical connector.




## -enum-fields




### -field COPP_ConnectorType_Unknown


            Unknown connector type.
          


### -field COPP_ConnectorType_VGA


            VGA (Video Graphics Array) connector.
          


### -field COPP_ConnectorType_SVideo


            S-Video connector.
          


### -field COPP_ConnectorType_CompositeVideo


            Composite video connector.
          


### -field COPP_ConnectorType_ComponentVideo


            Component video connector.
          


### -field COPP_ConnectorType_DVI


            DVI (digital video interface) connector.
          


### -field COPP_ConnectorType_HDMI


            HDMI (high-definition multimedia interface) connector.
          


### -field COPP_ConnectorType_LVDS


            LVDS (Low voltage differential signaling) connector.
          


### -field COPP_ConnectorType_TMDS


            Reserved.
          


### -field COPP_ConnectorType_D_JPN


            Japanese D connector. (Connector conforming to the EIAJ RC-5237 standard.)
          


### -field COPP_ConnectorType_Internal


            Internal connector. This flag can be combined with the other flags. This flag indicates that the connection between the graphics adapter and the display device is permanent and not accessible to the user.
          


### -field COPP_ConnectorType_ForceDWORD

Reserved. Do not use.


#### - COPP_ConnectorType_DisplayPortEmbedded

An embedded display port that connects internally to a display device. Also known as an <i>integrated</i> display port.

Applications should not enable High-Bandwidth Digital Content Protection (HDCP)  for embedded display ports.


#### - COPP_ConnectorType_DisplayPortExternal

A display port that connects externally to a display device


#### - COPP_ConnectorType_SDI


            Serial digital image connector.
          


#### - COPP_ConnectorType_UDIEmbedded

An embedded UDI that connects internally to a display device. Also known as an <i>integrated</i> UDI.


#### - COPP_ConnectorType_UDIExternal

A Unified Display Interface (UDI) that connects externally to a display device.


## -remarks



If a connector is described as <i>embedded</i> or <i>integrated</i>, it implies that the connector  is internal. These connectors have "Embedded" in the name of the enumeration constant. 

Applications should ignore the <b>COPP_ConnectorType_Internal</b> flag and instead check for connector types with "Embedded" in the constant name.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 


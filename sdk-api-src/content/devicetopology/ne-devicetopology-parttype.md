---
UID: NE:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0012
title: PartType (devicetopology.h)
description: The PartType enumeration defines constants that indicate whether a part in a device topology is a connector or subunit.helpviewer_keywords: ["Connector","PartType","PartType","PartType enumeration [Core Audio]","Subunit","coreaudio.parttype","devicetopology/Connector","devicetopology/PartType","devicetopology/Subunit"]
old-location: coreaudio\parttype.htm
tech.root: CoreAudio
ms.assetid: 7374d6c6-c59e-4862-8b4c-bbe384ccc9d8
ms.date: 12/05/2018
ms.keywords: Connector, PartType, PartType , PartType enumeration [Core Audio], Subunit, coreaudio.parttype, devicetopology/Connector, devicetopology/PartType, devicetopology/Subunit
f1_keywords:
- devicetopology/PartType
dev_langs:
- c++
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Devicetopology.h
api_name:
- PartType
targetos: Windows
req.typenames: PartType
req.redist: 
ms.custom: 19H1
---

# PartType enumeration


## -description



The <b>PartType</b> enumeration defines constants that indicate whether a part in a device topology is a connector or subunit.




## -enum-fields




### -field Connector

The part is a connector. A connector can represent an audio jack, an internal connection to an integrated endpoint device, or a software connection implemented through DMA transfers. For more information about connector types, see <a href="https://docs.microsoft.com/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType Enumeration</a>.


### -field Subunit

The part is a subunit. A subunit is an audio-processing node in a device topology. A subunit frequently has one or more hardware control parameters that can be set under program control. For example, an audio application can change the volume setting of a volume-control subunit.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getparttype">IPart::GetPartType</a> method uses the constants defined in the <b>PartType</b> enumeration to indicate whether an <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> object represents a connector or a subunit. If an <b>IPart</b> object represents a connector, a client can query that that object for its <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface. If an <b>IPart</b> object represents a subunit, a client can query that that object for its <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit</a> interface.

For more information about connectors and subunits, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-constants">Core Audio Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit Interface</a>
 

 


---
UID: NF:devicetopology.IDeviceTopology.GetConnectorCount
title: IDeviceTopology::GetConnectorCount
author: windows-sdk-content
description: The GetConnectorCount method gets the number of connectors in the device-topology object.
old-location: coreaudio\idevicetopology_getconnectorcount.htm
old-project: CoreAudio
ms.assetid: 0b7f3b14-4c99-497b-a00e-a24535a621b7
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetConnectorCount, GetConnectorCount method [Core Audio], GetConnectorCount method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetConnectorCount method, IDeviceTopology.GetConnectorCount, IDeviceTopology::GetConnectorCount, IDeviceTopologyGetConnectorCount, coreaudio.idevicetopology_getconnectorcount, devicetopology/IDeviceTopology::GetConnectorCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IDeviceTopology.GetConnectorCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDeviceTopology::GetConnectorCount


## -description



The <b>GetConnectorCount</b> method gets the number of connectors in the device-topology object.




## -parameters




### -param pCount [out]

Pointer to a <b>UINT</b> pointer variable into which the method writes the connector count (the number of connectors in the device topology).


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology Interface</a>
 

 


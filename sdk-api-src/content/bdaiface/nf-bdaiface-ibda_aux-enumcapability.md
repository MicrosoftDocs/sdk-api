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

# IBDA_AUX::EnumCapability


## -description


Gets the capabilities of an auxiliary connector, specified by index.


## -parameters




### -param dwIndex [in]

The zero-based index of the auxiliary connector. To get the number of connectors on the device, call <a href="https://msdn.microsoft.com/7bb80ae2-050e-4fe6-9dd4-9cc6b2bcdd3c">IBDA_AUX::QueryCapabilities</a>.


### -param dwInputID [out]

Receives a unique identifier for the auxiliary connector.


### -param pConnectorType [out]

Receives a GUID that specifies the type of connector.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBDA_AUX_CONNECTOR_TYPE_Composite"></a><a id="pbda_aux_connector_type_composite"></a><a id="PBDA_AUX_CONNECTOR_TYPE_COMPOSITE"></a><dl>
<dt><b>PBDA_AUX_CONNECTOR_TYPE_Composite</b></dt>
</dl>
</td>
<td width="60%">
Composite video connector.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_AUX_CONNECTOR_TYPE_SVideo"></a><a id="pbda_aux_connector_type_svideo"></a><a id="PBDA_AUX_CONNECTOR_TYPE_SVIDEO"></a><dl>
<dt><b>PBDA_AUX_CONNECTOR_TYPE_SVideo</b></dt>
</dl>
</td>
<td width="60%">
S-Video connector.

</td>
</tr>
</table>
 


### -param ConnTypeNum [out]

Receives a numeric identifier for the auxiliary input.


### -param NumVideoStds [out]

Receives the number of analog video standards that the connector supports.  


### -param AnalogStds [out]

Receives a bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration, specifying which analog video standards the connector supports.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://msdn.microsoft.com/7bb80ae2-050e-4fe6-9dd4-9cc6b2bcdd3c">IBDA_AUX::QueryCapabilities</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/8397a04f-5d40-4fa3-ac02-79c764abd174">IBDA_AUX</a>
 

 


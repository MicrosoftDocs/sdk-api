---
UID: NF:bdaiface.IBDA_AUX.EnumCapability
title: IBDA_AUX::EnumCapability
author: windows-driver-content
description: Gets the capabilities of an auxiliary connector, specified by index.
old-location: mstv\ibda_aux_enumcapability.htm
old-project: mstv
ms.assetid: 5f04c080-81c9-4aa9-ba54-5e16a538f10a
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: EnumCapability, EnumCapability method [Microsoft TV Technologies], EnumCapability method [Microsoft TV Technologies],IBDA_AUX interface, IBDA_AUX interface [Microsoft TV Technologies],EnumCapability method, IBDA_AUX.EnumCapability, IBDA_AUX::EnumCapability, PBDA_AUX_CONNECTOR_TYPE_Composite, PBDA_AUX_CONNECTOR_TYPE_SVideo, bdaiface/IBDA_AUX::EnumCapability, mstv.ibda_aux_enumcapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_AUX.EnumCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 


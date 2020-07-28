---
UID: NF:bdaiface.IBDA_AUX.EnumCapability
title: IBDA_AUX::EnumCapability (bdaiface.h)
description: Gets the capabilities of an auxiliary connector, specified by index.
helpviewer_keywords: ["EnumCapability","EnumCapability method [Microsoft TV Technologies]","EnumCapability method [Microsoft TV Technologies]","IBDA_AUX interface","IBDA_AUX interface [Microsoft TV Technologies]","EnumCapability method","IBDA_AUX.EnumCapability","IBDA_AUX::EnumCapability","PBDA_AUX_CONNECTOR_TYPE_Composite","PBDA_AUX_CONNECTOR_TYPE_SVideo","bdaiface/IBDA_AUX::EnumCapability","mstv.ibda_aux_enumcapability"]
old-location: mstv\ibda_aux_enumcapability.htm
tech.root: mstv
ms.assetid: 5f04c080-81c9-4aa9-ba54-5e16a538f10a
ms.date: 12/05/2018
ms.keywords: EnumCapability, EnumCapability method [Microsoft TV Technologies], EnumCapability method [Microsoft TV Technologies],IBDA_AUX interface, IBDA_AUX interface [Microsoft TV Technologies],EnumCapability method, IBDA_AUX.EnumCapability, IBDA_AUX::EnumCapability, PBDA_AUX_CONNECTOR_TYPE_Composite, PBDA_AUX_CONNECTOR_TYPE_SVideo, bdaiface/IBDA_AUX::EnumCapability, mstv.ibda_aux_enumcapability
f1_keywords:
- bdaiface/IBDA_AUX.EnumCapability
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdaiface.h
api_name:
- IBDA_AUX.EnumCapability
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_AUX::EnumCapability


## -description


Gets the capabilities of an auxiliary connector, specified by index.


## -parameters




### -param dwIndex [in]

The zero-based index of the auxiliary connector. To get the number of connectors on the device, call <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_aux-querycapabilities">IBDA_AUX::QueryCapabilities</a>.


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

Receives a bitwise <b>OR</b> of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration, specifying which analog video standards the connector supports.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_aux-querycapabilities">IBDA_AUX::QueryCapabilities</a> method before calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_aux">IBDA_AUX</a>
 

 


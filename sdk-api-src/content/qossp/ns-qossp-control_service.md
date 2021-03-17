---
UID: NS:qossp._CONTROL_SERVICE
title: CONTROL_SERVICE (qossp.h)
description: The CONTROL_SERVICE structure contains supported RSVP service types.
helpviewer_keywords: ["*LPCONTROL_SERVICE","*LPCONTROL_SERVICE structure [QOS]","CONTROL_SERVICE","CONTROL_SERVICE structure [QOS]","SERVICETYPE_BESTEFFORT","SERVICETYPE_CONTROLLEDLOAD","SERVICETYPE_GENERAL_INFORMATION","SERVICETYPE_GUARANTEED","SERVICETYPE_NETWORK_CONTROL","SERVICETYPE_NETWORK_UNAVAILABLE","SERVICETYPE_NOCHANGE","SERVICETYPE_NONCONFORMING","SERVICETYPE_NOTRAFFIC","SERVICETYPE_QUALITATIVE","qos.control_service","qossp/*LPCONTROL_SERVICE","qossp/CONTROL_SERVICE"]
old-location: qos\control_service.htm
tech.root: QOS
ms.assetid: 604d7be8-955b-40a3-9cb4-6cbfbeeaa105
ms.date: 12/05/2018
ms.keywords: '*LPCONTROL_SERVICE, *LPCONTROL_SERVICE structure [QOS], CONTROL_SERVICE, CONTROL_SERVICE structure [QOS], SERVICETYPE_BESTEFFORT, SERVICETYPE_CONTROLLEDLOAD, SERVICETYPE_GENERAL_INFORMATION, SERVICETYPE_GUARANTEED, SERVICETYPE_NETWORK_CONTROL, SERVICETYPE_NETWORK_UNAVAILABLE, SERVICETYPE_NOCHANGE, SERVICETYPE_NONCONFORMING, SERVICETYPE_NOTRAFFIC, SERVICETYPE_QUALITATIVE, qos.control_service, qossp/*LPCONTROL_SERVICE, qossp/CONTROL_SERVICE'
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: CONTROL_SERVICE, *LPCONTROL_SERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONTROL_SERVICE
 - qossp/_CONTROL_SERVICE
 - LPCONTROL_SERVICE
 - qossp/LPCONTROL_SERVICE
 - CONTROL_SERVICE
 - qossp/CONTROL_SERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - CONTROL_SERVICE
---

# CONTROL_SERVICE structure


## -description

The <b>CONTROL_SERVICE</b> structure contains supported RSVP service types.

## -struct-fields

### -field Length

Length of the entire structure, in bytes.

### -field Service

The supported service type. Must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOTRAFFIC"></a><a id="servicetype_notraffic"></a><dl>
<dt><b>SERVICETYPE_NOTRAFFIC</b></dt>
</dl>
</td>
<td width="60%">
No data is being sent in this direction.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_BESTEFFORT"></a><a id="servicetype_besteffort"></a><dl>
<dt><b>SERVICETYPE_BESTEFFORT</b></dt>
</dl>
</td>
<td width="60%">
Best Effort service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_CONTROLLEDLOAD"></a><a id="servicetype_controlledload"></a><dl>
<dt><b>SERVICETYPE_CONTROLLEDLOAD</b></dt>
</dl>
</td>
<td width="60%">
Controlled Load service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GUARANTEED"></a><a id="servicetype_guaranteed"></a><dl>
<dt><b>SERVICETYPE_GUARANTEED</b></dt>
</dl>
</td>
<td width="60%">
Guaranteed service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_UNAVAILABLE"></a><a id="servicetype_network_unavailable"></a><dl>
<dt><b>SERVICETYPE_NETWORK_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
This service type is used to notify the user that the network is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GENERAL_INFORMATION"></a><a id="servicetype_general_information"></a><dl>
<dt><b>SERVICETYPE_GENERAL_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
This service type corresponds to General Parameters, as defined by IntServ (the Integrated Services Working Group in the IETF).

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOCHANGE"></a><a id="servicetype_nochange"></a><dl>
<dt><b>SERVICETYPE_NOCHANGE</b></dt>
</dl>
</td>
<td width="60%">
This specifies that the flow specification contains no changes from the previous specification.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NONCONFORMING"></a><a id="servicetype_nonconforming"></a><dl>
<dt><b>SERVICETYPE_NONCONFORMING</b></dt>
</dl>
</td>
<td width="60%">
Specifies non-conforming traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_CONTROL"></a><a id="servicetype_network_control"></a><dl>
<dt><b>SERVICETYPE_NETWORK_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
Specifies network control traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_QUALITATIVE"></a><a id="servicetype_qualitative"></a><dl>
<dt><b>SERVICETYPE_QUALITATIVE</b></dt>
</dl>
</td>
<td width="60%">
Qualitative service.

</td>
</tr>
</table>

### -field Overrides

Specifies overrides to service specifications, expressed in the form of an <a href="/windows/desktop/api/qossp/ns-qossp-ad_general_params">AD_GENERAL_PARAMS</a> structure.

### -field Guaranteed

Specifies guaranteed service, and provides service parameters in the form of an <b>AD_GUARANTEED</b> structure.

### -field ParamBuffer

Describes the buffer used, in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-param_buffer">PARAM_BUFFER</a> structure.

## -remarks

The <b>Length</b> value can be added to the pointer to the structure to obtain the pointer to the next <b>CONTROL_SERVICE</b> structure in the list, until the <b>NumberOfServices</b> member of the <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_adspec">RSVP_ADSPEC</a> structure is exhausted.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-param_buffer">PARAM_BUFFER</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_adspec">RSVP_ADSPEC</a>
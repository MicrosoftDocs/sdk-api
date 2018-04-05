---
UID: NE:vdshwprv._VDS_TRANSITION_STATE
title: "_VDS_TRANSITION_STATE"
author: windows-driver-content
description: Defines the set of the valid transition state values for a VDS object.
old-location: base\vds_transition_state.htm
old-project: VDS
ms.assetid: ef688d1f-136b-4bc8-8209-e30033e752e9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VDS_TRANSITION_STATE, VDS_TRANSITION_STATE enumeration, VDS_TS_EXTENDING, VDS_TS_RECONFIGING, VDS_TS_RESTRIPING, VDS_TS_SHRINKING, VDS_TS_STABLE, VDS_TS_UNKNOWN, _VDS_TRANSITION_STATE, base.vds_transition_state, vds/VDS_TRANSITION_STATE, vds/VDS_TS_EXTENDING, vds/VDS_TS_RECONFIGING, vds/VDS_TS_RESTRIPING, vds/VDS_TS_SHRINKING, vds/VDS_TS_STABLE, vds/VDS_TS_UNKNOWN, vdshwprv/VDS_TRANSITION_STATE, vdshwprv/VDS_TS_EXTENDING, vdshwprv/VDS_TS_RECONFIGING, vdshwprv/VDS_TS_RESTRIPING, vdshwprv/VDS_TS_SHRINKING, vdshwprv/VDS_TS_STABLE, vdshwprv/VDS_TS_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VDS_TRANSITION_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_TRANSITION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_TRANSITION_STATE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the set of the valid transition state values for a VDS object.


## -enum-fields




### -field VDS_TS_UNKNOWN

This value is reserved.


### -field VDS_TS_STABLE

The object is stable. No configuration activity is currently in progress.


### -field VDS_TS_EXTENDING

The object is being extended.


### -field VDS_TS_SHRINKING

The object is being shrunk.


### -field VDS_TS_RECONFIGING

The object is being automagically reconfigured.


### -field VDS_TS_RESTRIPING

The object is being restriped.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



Transition state enumeration values apply to the VDS objects as shown in the following table. Y indicates that the value 
    applies to the object, and N indicates that the value does not apply to the object. 

<table>
<tr>
<th>Transition state enumeration value</th>
<th>LUN</th>
<th>LUN plex</th>
<th>Volume</th>
<th>Volume plex</th>
</tr>
<tr>
<td><b>VDS_TS_UNKNOWN</b></td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_TS_STABLE</b></td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_TS_EXTENDING</b></td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_TS_SHRINKING</b></td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_TS_RECONFIGING</b></td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_TS_RESTRIPING</b></td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
</table>
 

The <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a>, 
    <a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>, 
    <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>, <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a>, and 
    <a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a> structures include a <b>VDS_TRANSITION_STATE</b> 
    value as a member to report the transition state of each object.

If your application encounters a <b>VDS_TRANSITION_STATE</b> value that it does not recognize, it should display the transition state as unknown. It should not attempt to map the unrecognized transition state to another transition state.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_TRANSITION_STATE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_TRANSITION_STATE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a>



<a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a>
 

 


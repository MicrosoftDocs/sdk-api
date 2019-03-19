---
UID: NS:fwpmtypes.FWPM_ACTION0_
title: FWPM_ACTION0 (fwpmtypes.h)
author: windows-sdk-content
description: Specifies the action taken if all the filter conditions are true.
old-location: fwp\fwpm_action0_struct.htm
tech.root: fwp
ms.assetid: 070e1324-d41d-4001-bf26-97465bf87f98
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_ACTION0, FWPM_ACTION0 structure [Filtering], FWP_ACTION_BLOCK, FWP_ACTION_CALLOUT_INSPECTION, FWP_ACTION_CALLOUT_TERMINATING, FWP_ACTION_CALLOUT_UNKNOWN, FWP_ACTION_PERMIT, fwp.fwpm_action0_struct, fwpmtypes/FWPM_ACTION0
ms.topic: struct
req.header: fwpmtypes.h
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
 - Fwpmtypes.h
api_name:
 - FWPM_ACTION0
product: Windows
targetos: Windows
req.typenames: FWPM_ACTION0
req.redist: 
---

# FWPM_ACTION0 structure


## -description


The <b>FWPM_ACTION0</b> structure specifies the action taken if all the filter conditions are true. 


## -struct-fields




### -field type

Action type as specified by <b>FWP_ACTION_TYPE</b> which maps to a <b>UINT32</b>.

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWP_ACTION_BLOCK"></a><a id="fwp_action_block"></a><dl>
<dt><b>FWP_ACTION_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
Block the traffic. 

0x00000001 | FWP_ACTION_FLAG_TERMINATING

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_ACTION_PERMIT"></a><a id="fwp_action_permit"></a><dl>
<dt><b>FWP_ACTION_PERMIT</b></dt>
</dl>
</td>
<td width="60%">
Permit the traffic.

0x00000002 | FWP_ACTION_FLAG_TERMINATING

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_ACTION_CALLOUT_TERMINATING"></a><a id="fwp_action_callout_terminating"></a><dl>
<dt><b>FWP_ACTION_CALLOUT_TERMINATING</b></dt>
</dl>
</td>
<td width="60%">
Invoke a callout that always returns block or permit.

0x00000003 | FWP_ACTION_FLAG_CALLOUT | FWP_ACTION_FLAG_TERMINATING

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_ACTION_CALLOUT_INSPECTION"></a><a id="fwp_action_callout_inspection"></a><dl>
<dt><b>FWP_ACTION_CALLOUT_INSPECTION</b></dt>
</dl>
</td>
<td width="60%">
Invoke a callout that never returns block or permit.

0x00000004 | FWP_ACTION_FLAG_CALLOUT | FWP_ACTION_FLAG_NON_TERMINATING

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_ACTION_CALLOUT_UNKNOWN"></a><a id="fwp_action_callout_unknown"></a><dl>
<dt><b>FWP_ACTION_CALLOUT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Invoke a callout that may return block or permit.

0x00000005 | FWP_ACTION_FLAG_CALLOUT

</td>
</tr>
</table>
 


### -field filterType

An arbitrary GUID chosen by the policy provider.

Available when the action does not invoke a callout, that is, <b>type</b> does not contain  <b>FWP_ACTION_FLAG_CALLOUT</b>.


### -field calloutKey

The GUID for a valid callout in the layer.

Available when the action invokes a callout, that is, <b>type</b> contains  <b>FWP_ACTION_FLAG_CALLOUT</b>.


### -field bitmapIndex

 




## -remarks



<b>FWPM_ACTION0</b> is a specific implementation of FWPM_ACTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 


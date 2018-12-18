---
UID: NS:mmeapi.tagMIXERCONTROLDETAILS_LISTTEXTW
title: MIXERCONTROLDETAILS_LISTTEXTW
author: windows-sdk-content
description: The MIXERCONTROLDETAILS structure refers to control-detail structures, retrieving or setting state information of an audio mixer control.
old-location: multimedia\mixercontroldetails.htm
tech.root: Multimedia
ms.assetid: 171605e0-4bfc-47cf-b667-3e73c172aebd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPMIXERCONTROLDETAILS_LISTTEXTW, *PMIXERCONTROLDETAILS_LISTTEXTW, 0, 1, MIXERCONTROL cMultipleItems member, MIXERCONTROLDETAILS, MIXERCONTROLDETAILS hwndOwner member, MIXERCONTROLDETAILS structure [Windows Multimedia], MIXERCONTROLDETAILS_BOOLEAN, MIXERCONTROLDETAILS_LISTTEXT, MIXERCONTROLDETAILS_LISTTEXTW, MIXERCONTROLDETAILS_SIGNED, MIXERCONTROLDETAILS_UNSIGNED, MIXERLINE cChannels, _win32_MIXERCONTROLDETAILS_str, mmeapi/MIXERCONTROLDETAILS, multimedia.mixercontroldetails, tMIXERCONTROLDETAILS"
ms.topic: struct
req.header: mmeapi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MIXERCONTROLDETAILS
product: Windows
targetos: Windows
req.typenames: MIXERCONTROLDETAILS_LISTTEXTW, *PMIXERCONTROLDETAILS_LISTTEXTW, *LPMIXERCONTROLDETAILS_LISTTEXTW
req.redist: 
---

# MIXERCONTROLDETAILS_LISTTEXTW structure


## -description



The <b>MIXERCONTROLDETAILS</b> structure refers to control-detail structures, retrieving or setting state information of an audio mixer control. All members of this structure must be initialized before calling the <a href="https://msdn.microsoft.com/b1fdd9e7-42cf-41fb-99f7-b7da990e5881">mixerGetControlDetails</a> and <a href="https://msdn.microsoft.com/c4d500f3-a1c2-432c-9096-90f229bc7b7a">mixerSetControlDetails</a> functions.




## -struct-fields




### -field dwParam1

 


### -field dwParam2

 


### -field szName

 




#### - cChannels

Number of channels on which to get or set control properties. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Use this value when the control is a MIXERCONTROL_CONTROLTYPE_CUSTOM control.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Use this value when the control is a MIXERCONTROL_CONTROLF_UNIFORM control or when an application needs to get and set all channels as if they were uniform.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_cChannels"></a><a id="mixerline_cchannels"></a><a id="MIXERLINE_CCHANNELS"></a><dl>
<dt><b>MIXERLINE cChannels</b></dt>
</dl>
</td>
<td width="60%">
Use this value when the properties for the control are expected on all channels for a line.

</td>
</tr>
</table>
 

An application cannot specify a value that falls between 1 and the number of channels for the audio line. For example, specifying 2 or 3 for a four-channel line is not valid. This member cannot be 0 for noncustom control types.


This member cannot be 0 for noncustom control types.


#### - cMultipleItems

Number of multiple items per channel on which to get or set properties. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Use this value for all controls except for a MIXERCONTROL_CONTROLF_MULTIPLE or a MIXERCONTROL_CONTROLTYPE_CUSTOM control.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_cMultipleItems_member"></a><a id="mixercontrol_cmultipleitems_member"></a><a id="MIXERCONTROL_CMULTIPLEITEMS_MEMBER"></a><dl>
<dt><b>MIXERCONTROL cMultipleItems member</b></dt>
</dl>
</td>
<td width="60%">
Use this value when the control class is MIXERCONTROL_CONTROLF_MULTIPLE.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROLDETAILS_hwndOwner_member"></a><a id="mixercontroldetails_hwndowner_member"></a><a id="MIXERCONTROLDETAILS_HWNDOWNER_MEMBER"></a><dl>
<dt><b>MIXERCONTROLDETAILS hwndOwner member</b></dt>
</dl>
</td>
<td width="60%">
Use this value when the control is a MIXERCONTROL_CONTROLTYPE_CUSTOM control and the MIXER_SETCONTROLDETAILSF_CUSTOM flag is specified for the mixerSetControlDetails function. 

In this case, the hwndOwner member overlaps with cMultipleItems, providing the value of the window handle.

</td>
</tr>
</table>
 

When using a MIXERCONTROL_CONTROLTYPE_CUSTOM control without the MIXERCONTROL_CONTROLTYPE_CUSTOM flag, specify zero for this member.

An application cannot specify any value other than the value specified in the cMultipleItems member of the MIXERCONTROL structure for a MIXERCONTROL_CONTROLF_MULTIPLE control.


#### - cbDetails

Size, in bytes, of one of the following details structures being used:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROLDETAILS_BOOLEAN"></a><a id="mixercontroldetails_boolean"></a><dl>
<dt><b>MIXERCONTROLDETAILS_BOOLEAN</b></dt>
</dl>
</td>
<td width="60%">
Boolean value for an audio line control.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROLDETAILS_LISTTEXT"></a><a id="mixercontroldetails_listtext"></a><dl>
<dt><b>MIXERCONTROLDETAILS_LISTTEXT</b></dt>
</dl>
</td>
<td width="60%">
List text buffer for an audio line control. For information about the appropriate details structure for a specific control, see <a href="https://msdn.microsoft.com/7d109d0e-360f-4a09-8498-15d37d6766b3">Control Types</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROLDETAILS_SIGNED"></a><a id="mixercontroldetails_signed"></a><dl>
<dt><b>MIXERCONTROLDETAILS_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
Signed value for an audio line control.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROLDETAILS_UNSIGNED"></a><a id="mixercontroldetails_unsigned"></a><dl>
<dt><b>MIXERCONTROLDETAILS_UNSIGNED</b></dt>
</dl>
</td>
<td width="60%">
Unsigned value for an audio line control.

</td>
</tr>
</table>
 


#### - cbStruct

Size, in bytes, of the <b>MIXERCONTROLDETAILS</b> structure. The size must be large enough to contain the base <b>MIXERCONTROLDETAILS</b> structure. When <a href="https://msdn.microsoft.com/b1fdd9e7-42cf-41fb-99f7-b7da990e5881">mixerGetControlDetails</a> returns, this member contains the actual size of the information returned. The returned information will not exceed the requested size, nor will it be smaller than the base <b>MIXERCONTROLDETAILS</b> structure.


#### - dwControlID

Control identifier on which to get or set properties.


#### - hwndOwner

Handle to the window that owns a custom dialog box for a mixer control. This member is used when the MIXER_SETCONTROLDETAILSF_CUSTOM flag is specified in the <a href="https://msdn.microsoft.com/c4d500f3-a1c2-432c-9096-90f229bc7b7a">mixerSetControlDetails</a> function.


#### - paDetails

Pointer to an array of one or more structures in which properties for 
				the specified control are retrieved or set. 

For MIXERCONTROL_CONTROLF_MULTIPLE controls, the size of this buffer should be the product of the <b>cChannels</b>, <b>cMultipleItems</b> and <b>cbDetails</b> members of the <b>MIXERCONTROLDETAILS</b> structure. For controls other than MIXERCONTROL_CONTROLF_MULTIPLE types, the size of this buffer is the product of the <b>cChannels</b> and <b>cbDetails</b> members of the <b>MIXERCONTROLDETAILS</b> structure.

For controls other than MIXERCONTROL_CONTROLF_MULTIPLE types, the size of this buffer is the product of the <b>cChannels</b> and <b>cbDetails</b> members of the <b>MIXERCONTROLDETAILS</b> structure. For controls other than MIXERCONTROL_CONTROLF_MULTIPLE types, the size of this buffer is the product of the <b>cChannels</b> and <b>cbDetails</b> members of the <b>MIXERCONTROLDETAILS</b> structure.

For controls that are MIXERCONTROL_CONTROLF_MULTIPLE types, the array can be treated as a two-dimensional array that is channel major. That is, all multiple items for the left channel are given, then all multiple items for the right channel, and so on.

For controls other than MIXERCONTROL_CONTROLF_MULTIPLE types, each element index is equivalent to the zero-based channel that it affects. That is, paDetails[0] is for the left channel and paDetails[1] is for the right channel.

If the control is a MIXERCONTROL_CONTROLTYPE_CUSTOM control, this member must point to a buffer that is at least large enough to contain the size, in bytes, specified by the cbCustomData member of the MIXERCONTROL structure.


## -see-also




<a href="https://msdn.microsoft.com/82101519-6906-45fd-908f-137e51a56fb8">Audio Mixer Structures</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>



<a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a>



<a href="https://msdn.microsoft.com/b1fdd9e7-42cf-41fb-99f7-b7da990e5881">mixerGetControlDetails</a>



<a href="https://msdn.microsoft.com/c4d500f3-a1c2-432c-9096-90f229bc7b7a">mixerSetControlDetails</a>
 

 


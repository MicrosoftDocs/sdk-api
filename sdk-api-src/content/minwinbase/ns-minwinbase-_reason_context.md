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

# _REASON_CONTEXT structure


## -description


Contains information about a power request. This structure is used by the 
    <a href="https://msdn.microsoft.com/2122bf00-9e6b-48ab-89b0-f53dd6804902">PowerCreateRequest</a> and 
    <a href="https://msdn.microsoft.com/2facde72-6e04-4a2f-9ee6-059f36932539">SetWaitableTimerEx</a> functions.


## -struct-fields




### -field Version

The version number of the structure. This parameter must be set to 
      <b>POWER_REQUEST_CONTEXT_VERSION</b>.


### -field Flags

The format of the reason for the power request. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POWER_REQUEST_CONTEXT_DETAILED_STRING"></a><a id="power_request_context_detailed_string"></a><dl>
<dt><b>POWER_REQUEST_CONTEXT_DETAILED_STRING</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <i>Detailed</i> structure identifies a localizable string resource that describes 
        the reason for the power request. 

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_REQUEST_CONTEXT_SIMPLE_STRING"></a><a id="power_request_context_simple_string"></a><dl>
<dt><b>POWER_REQUEST_CONTEXT_SIMPLE_STRING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <i>SimpleReasonString</i> parameter contains a simple, non-localizable string that 
        describes the reason for the power request.

</td>
</tr>
</table>
 


### -field Reason

A union that consists of either a <b>Detailed</b> structure or a string.  


### -field Reason.Detailed

A structure that identifies a localizable string resource to describe the reason for the power 
       request.


### -field Reason.Detailed.LocalizedReasonModule

The module that contains the string resource.


### -field Reason.Detailed.LocalizedReasonId

The ID of the string resource.


### -field Reason.Detailed.ReasonStringCount

The number of strings in the <i>ReasonStrings</i> parameter.


### -field Reason.Detailed.ReasonStrings

An array of strings to be substituted in the string resource at run time. 


### -field Reason.SimpleReasonString

A non-localized string that describes the reason for the power request.  


## -see-also




<a href="https://msdn.microsoft.com/2122bf00-9e6b-48ab-89b0-f53dd6804902">PowerCreateRequest</a>



<a href="https://msdn.microsoft.com/2facde72-6e04-4a2f-9ee6-059f36932539">SetWaitableTimerEx</a>
 

 


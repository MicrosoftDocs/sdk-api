---
UID: NS:minwinbase._REASON_CONTEXT
title: "_REASON_CONTEXT"
author: windows-driver-content
description: Contains information about a power request. This structure is used by the PowerCreateRequest and SetWaitableTimerEx functions.
old-location: base\reason_context.htm
old-project: Power
ms.assetid: 006bb84f-5e51-4f6e-8a44-6b50e763c5ca
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PREASON_CONTEXT, POWER_REQUEST_CONTEXT_DETAILED_STRING, POWER_REQUEST_CONTEXT_SIMPLE_STRING, PREASON_CONTEXT, PREASON_CONTEXT structure pointer, REASON_CONTEXT, REASON_CONTEXT structure, _REASON_CONTEXT, base.reason_context, minwinbase/PREASON_CONTEXT, minwinbase/REASON_CONTEXT, winbase/PREASON_CONTEXT, winbase/REASON_CONTEXT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REASON_CONTEXT, *PREASON_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MinWinBase.h
-	WinBase.h
api_name:
-	REASON_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 


---
UID: NF:recapis.CloneContext
title: CloneContext function
author: windows-driver-content
description: Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original.
old-location: tablet\clonecontext.htm
old-project: tablet
ms.assetid: 0a16d012-1d88-4dfb-a1a0-44a842d9ee1d
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 0a16d012-1d88-4dfb-a1a0-44a842d9ee1d, CloneContext, CloneContext function [Tablet PC], recapis/CloneContext, tablet.clonecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	recapis.h
api_name:
-	CloneContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CloneContext function


## -description



Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pCloneHrc

The new recognizer context.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCloneHrc</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -remarks



The settings  for this context include the recognition guide, character Autocomplete mode, and any factoids that improve the recognition results. An example of a factoid may include whether the ink is a phone number, a name, or a URL. The TextContext and Wordlists are preserved in the new context.






## -see-also




<a href="https://msdn.microsoft.com/92446aca-e611-42b2-8b55-2d1c47ccaa5c">ResetContext Function</a>



<a href="https://msdn.microsoft.com/f5461326-3def-4564-81ea-32a63b889da0">SetTextContext Function</a>
 

 


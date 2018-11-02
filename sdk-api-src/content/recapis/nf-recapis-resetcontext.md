---
UID: NF:recapis.ResetContext
title: ResetContext function
author: windows-sdk-content
description: Deletes the current ink and recognition results from the context.The current settings of the recognizer context are preserved.
old-location: tablet\resetcontext.htm
tech.root: tablet
ms.assetid: 92446aca-e611-42b2-8b55-2d1c47ccaa5c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 92446aca-e611-42b2-8b55-2d1c47ccaa5c, ResetContext, ResetContext function [Tablet PC], recapis/ResetContext, tablet.resetcontext
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - ResetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResetContext function


## -description



Deletes the current ink and recognition results from the context.

The current settings of the recognizer context are preserved. The settings can include the recognition guide, character Autocomplete mode, and any recognition hints that improve recognition results. An example of a recognition hint may include whether a factoid is set indicating that the ink is a phone number, a name, or a URL. The TextContext and Wordlists are preserved in the context.




## -parameters




### -param hrc

The handle to the recognizer context.


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
 




## -see-also




<a href="https://msdn.microsoft.com/0a16d012-1d88-4dfb-a1a0-44a842d9ee1d">CloneContext Function</a>
 

 


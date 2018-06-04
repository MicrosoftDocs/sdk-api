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

# FilterReplyMessage function


## -description


The <b>FilterReplyMessage</b> function replies to a message from a kernel-mode minifilter. 


## -parameters




### -param hPort [in]

Communication port handle returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>. This parameter is required and cannot be <b>NULL</b>. 


### -param lpReplyBuffer [in]

A pointer to a caller-allocated buffer containing the reply to be sent to the minifilter. The reply must contain a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541628">FILTER_REPLY_HEADER</a> structure, but otherwise, its format is caller-defined. This parameter is required and cannot be <b>NULL</b>. 


### -param dwReplyBufferSize [in]

Size, in bytes, of the buffer that the <i>lpReplyBuffer</i> parameter points to. See the Remarks section.


## -returns



<b>FilterReplyMessage</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



A user-mode application calls the <b>FilterReplyMessage</b> function to reply to a message received from a kernel-mode minifilter. 

To get a message from a minifilter, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540506">FilterGetMessage</a>. 

To send a message to a minifilter, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff541513">FilterSendMessage</a>. 

A minifilter sends a message to a user-mode application by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a>. 

<div class="alert"><b>Important</b>    Due to (system-specific) structure <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">padding</a> requirements, accuracy is required when you set the size of buffers that are associated with <a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a> and <b>FilterReplyMessage</b>. As an example, assume data must be sent (via <b>FilterReplyMessage</b>) to a minifilter.  The user-mode component might declare the following structure to do so:<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct _REPLY_STRUCT
{
     FILTER_REPLY_HEADER Header;
     MY_STRUCTURE Data;  // The structure to be sent to the minifilter.
} REPLY_STRUCT, *PREPLY_STRUCT;</pre>
</td>
</tr>
</table></span></div>
<p class="note">Given this structure, it might seem obvious that the caller of <b>FilterReplyMessage</b> would set the <i>dwReplyBufferSize</i> parameter to <code>sizeof(REPLY_STRUCT)</code> and the <i>ReplyLength</i> parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a> to the same value.  However, because of structure padding idiosyncrasies, <code>sizeof(REPLY_STRUCT)</code> might be larger than <code>sizeof(FILTER_REPLY_HEADER) + sizeof(MY_STRUCT)</code>.  If this is the case, <b>FltSendMessage</b> returns STATUS_BUFFER_OVERFLOW.

<p class="note">Therefore, we recommend that you call <b>FilterReplyMessage</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a> (leveraging the above example) by setting <i>dwReplyBufferSize</i> and <i>ReplyLength</i> both to <code>sizeof(FILTER_REPLY_HEADER) + sizeof(MY_STRUCT)</code> instead of <code>sizeof(REPLY_STRUCT)</code>. This ensures that any extra padding at the end of the <b>REPLY_STRUCT</b> structure is ignored.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541628">FILTER_REPLY_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540460">FilterConnectCommunicationPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540506">FilterGetMessage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541513">FilterSendMessage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544378">FltSendMessage</a>
 

 


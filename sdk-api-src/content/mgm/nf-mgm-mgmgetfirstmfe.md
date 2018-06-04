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

# MgmGetFirstMfe function


## -description


The 
<b>MgmGetFirstMfe</b> function retrieves MFEs starting at the beginning of the MFE list. The function can retrieve zero, one, or more MFEs. The number of MFEs returned depends on the size of the MFEs and the size of the buffer supplied by the client when the function is called.

The data returned in the buffer is ordered first by group, and then by the sources within a group.


## -parameters




### -param pdwBufferSize [in, out]

On input, <i>pdwBufferSize</i> is a pointer to a <b>DWORD</b>-sized memory location containing the size, in bytes, of <i>pbBuffer</i>. 




On output, if the return value is ERROR_INSUFFICIENT_BUFFER, <i>pdwBufferSize</i> receives the minimum size <i>pbBuffer</i> must be to hold the MFE; otherwise, the value of <i>pdwBufferSize</i> remains unchanged.


### -param pbBuffer [in, out]

On input, the client must supply a pointer to a buffer. 




On output, <i>pbBuffer</i> contains one or more MFEs. Each MFE is a 
<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a> structure.


### -param pdwNumEntries [in, out]

On input, the client must supply a pointer to a <b>DWORD</b>-sized memory location. 




On output, <i>pdwNumEntries</i> receives the number of MFEs contained in <i>pbBuffer</i>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The specified buffer is too small for even one MFE. The client should check the value of <i>pdwBufferSize</i> for the minimum buffer size required to retrieve one MFE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More MFEs are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more MFEs are available. Zero or more MFEs were returned; check the value of <i>pdwNumEntries</i> to verify how many MFEs were returned.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This function is used to begin sequential retrieval of MFEs; use 
<a href="https://msdn.microsoft.com/067003ef-bb92-48cc-bc13-5b90066c9123">MgmGetNextMfe</a> to continue the retrieval process.

In general, to retrieve MFEs, first call 
<b>MgmGetFirstMfe</b>. Then, call 
<a href="https://msdn.microsoft.com/067003ef-bb92-48cc-bc13-5b90066c9123">MgmGetNextMfe</a> one or more times, until there are no more MFEs to return. Each call to 
<b>MgmGetNextMfe</b> should begin after the last MFE returned by the previous call to 
<b>MgmGetNextMfe</b> (or the initial call to 
<b>MgmGetFirstMfe</b>). To do this, the client specifies the last source and group in the buffer returned by a previous call.

<div class="alert"><b>Note</b>  The minimum size of the buffer pointed to by <i>pbBuffer</i> is not fixed; it is different for each MFE. Use the 
sizeof(<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a>) macro to determine the size of each MFE returned in the buffer.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a>



<a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a>



<a href="https://msdn.microsoft.com/067003ef-bb92-48cc-bc13-5b90066c9123">MgmGetNextMfe</a>
 

 


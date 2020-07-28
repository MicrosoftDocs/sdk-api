---
UID: NF:mgm.MgmGetFirstMfe
title: MgmGetFirstMfe function (mgm.h)
description: The MgmGetFirstMfe function retrieves MFEs starting at the beginning of the MFE list.
helpviewer_keywords: ["MgmGetFirstMfe","MgmGetFirstMfe function [RAS]","_mpr_mgmgetfirstmfe","mgm/MgmGetFirstMfe","rras.mgmgetfirstmfe"]
old-location: rras\mgmgetfirstmfe.htm
tech.root: RRAS
ms.assetid: b270efc9-479c-4f70-a29d-1fee269c4f30
ms.date: 12/05/2018
ms.keywords: MgmGetFirstMfe, MgmGetFirstMfe function [RAS], _mpr_mgmgetfirstmfe, mgm/MgmGetFirstMfe, rras.mgmgetfirstmfe
f1_keywords:
- mgm/MgmGetFirstMfe
dev_langs:
- c++
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Rtm.dll
api_name:
- MgmGetFirstMfe
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure.


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
<a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetnextmfe">MgmGetNextMfe</a> to continue the retrieval process.

In general, to retrieve MFEs, first call 
<b>MgmGetFirstMfe</b>. Then, call 
<a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetnextmfe">MgmGetNextMfe</a> one or more times, until there are no more MFEs to return. Each call to 
<b>MgmGetNextMfe</b> should begin after the last MFE returned by the previous call to 
<b>MgmGetNextMfe</b> (or the initial call to 
<b>MgmGetFirstMfe</b>). To do this, the client specifies the last source and group in the buffer returned by a previous call.

<div class="alert"><b>Note</b>  The minimum size of the buffer pointed to by <i>pbBuffer</i> is not fixed; it is different for each MFE. Use the 
sizeof(<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a>) macro to determine the size of each MFE returned in the buffer.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetmfe">MgmGetMfe</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetnextmfe">MgmGetNextMfe</a>
 

 


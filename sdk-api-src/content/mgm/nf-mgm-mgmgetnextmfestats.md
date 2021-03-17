---
UID: NF:mgm.MgmGetNextMfeStats
title: MgmGetNextMfeStats function (mgm.h)
description: The MgmGetNextMfeStats function retrieves one or more sets of MFE statistics.
helpviewer_keywords: ["MGM_MFE_STATS_0","MGM_MFE_STATS_1","MgmGetNextMfeStats","MgmGetNextMfeStats function [RAS]","_mpr_mgmgetnextmfestats","mgm/MgmGetNextMfeStats","rras.mgmgetnextmfestats"]
old-location: rras\mgmgetnextmfestats.htm
tech.root: RRAS
ms.assetid: af8dd38e-e66f-459a-a07c-c298154901f6
ms.date: 12/05/2018
ms.keywords: MGM_MFE_STATS_0, MGM_MFE_STATS_1, MgmGetNextMfeStats, MgmGetNextMfeStats function [RAS], _mpr_mgmgetnextmfestats, mgm/MgmGetNextMfeStats, rras.mgmgetnextmfestats
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MgmGetNextMfeStats
 - mgm/MgmGetNextMfeStats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmGetNextMfeStats
---

# MgmGetNextMfeStats function


## -description

The 
<b>MgmGetNextMfeStats</b> function retrieves one or more sets of MFE statistics. The routing table manager starts retrieving statistics starting with the MFE that follows the specified MFE. The function can retrieve zero, one, or more sets of MFE statistics. The number of sets returned depends on the size of the entries and the size of the buffer supplied by the client when the function is called.

The data returned in the buffer is ordered first by group, and then by the sources within a group. The statistics returned include the packets received, bytes received, and packets forwarded on each outgoing interface.

## -parameters

### -param pimmStart [in]

Pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure that specifies from where to begin retrieving MFE statistics. The <b>dwSource</b> and <b>dwGroup</b> members of the 
<b>MIB_IPMCAST_MFE</b> structure identify an MFE. Specify the source and group of the last MFE that was returned by the previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfestats">MgmGetFirstMfeStats</a> or 
<b>MgmGetNextMfeStats</b>.

### -param pdwBufferSize [in, out]

On input, <i>pdwBufferSize</i> is a pointer to a <b>DWORD</b>-sized memory location that contains the size, in bytes, of <i>pbBuffer</i>. 




On output, if the return value is <b>ERROR_INSUFFICIENT_BUFFER</b>, <i>pdwBufferSize</i> receives the minimum size <i>pbBuffer</i> must be to hold a set of MFE statistics; otherwise, the value of <i>pdwBufferSize</i> remains unchanged.

### -param pbBuffer [in, out]

On input, the client must supply a pointer to a buffer. 




On output, <i>pbBuffer</i> contains one or more sets of MFE statistics. Each set of MFE statistics is a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a> structure.

### -param pdwNumEntries [in, out]

On input, the client must supply a pointer to a <b>DWORD</b>-sized memory location. 




On output, <i>pdwNumEntries</i> receives the number of sets of MFE statistics contained in <i>pbBuffer</i>.

### -param dwFlags

Determines the data structure returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MGM_MFE_STATS_0"></a><a id="mgm_mfe_stats_0"></a><dl>
<dt><b>MGM_MFE_STATS_0</b></dt>
</dl>
</td>
<td width="60%">
Include statistics corresponding to <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MGM_MFE_STATS_1"></a><a id="mgm_mfe_stats_1"></a><dl>
<dt><b>MGM_MFE_STATS_1</b></dt>
</dl>
</td>
<td width="60%">
Include statistics corresponding to <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a>.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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
The specified buffer is too small for even one set of MFE statistics. The client should check the value of <i>pdwBufferSize</i> for the minimum buffer size required to retrieve one set of statistics.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More MFE statistics are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more MFE statistics are available. Zero or more sets of MFE statistics were returned; check the value of <i>pdwNumEntries</i> to verify how many sets of statistics were returned.

</td>
</tr>
</table>

## -remarks

This function is used to continue the sequential retrieval of MFE statistics; use 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfestats">MgmGetFirstMfeStats</a> to start the retrieval process.

In general, to retrieve MFE statistics, first call 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfestats">MgmGetFirstMfeStats</a>. Then, call 
<b>MgmGetNextMfeStats</b> one or more times, until there are no more MFEs to return. Each call to 
<b>MgmGetNextMfeStats</b> should begin after the last MFE returned by the previous call to 
<b>MgmGetNextMfeStats</b> (or the initial call to 
<b>MgmGetFirstMfeStats</b>) To do this, the client specifies the last source and group in the buffer returned by a previous call.

The MFE statistics are returned in either an <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a> or <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a> structure determined by the <i>dwFlags</i> parameter.

<div class="alert"><b>Note</b>  The minimum size of the buffer pointed to by <i>pbBuffer</i> is not fixed; it is different for each set of MFE statistics. Use the 
<b>sizeof</b> macro to determine the size of each set of statistics returned in the buffer.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfestats">MgmGetFirstMfeStats</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetmfestats">MgmGetMfeStats</a>
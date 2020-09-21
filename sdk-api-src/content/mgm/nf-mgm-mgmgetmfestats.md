---
UID: NF:mgm.MgmGetMfeStats
title: MgmGetMfeStats function (mgm.h)
description: The MgmGetMfeStats function retrieves the statistics for a specific MFE. The statistics returned include the packets received, bytes received, and the packets forwarded on each outgoing interface.
helpviewer_keywords: ["MGM_MFE_STATS_0","MGM_MFE_STATS_1","MgmGetMfeStats","MgmGetMfeStats function [RAS]","_mpr_mgmgetmfestats","mgm/MgmGetMfeStats","rras.mgmgetmfestats"]
old-location: rras\mgmgetmfestats.htm
tech.root: RRAS
ms.assetid: 16c4b403-0477-47da-9f98-55f8368dca15
ms.date: 12/05/2018
ms.keywords: MGM_MFE_STATS_0, MGM_MFE_STATS_1, MgmGetMfeStats, MgmGetMfeStats function [RAS], _mpr_mgmgetmfestats, mgm/MgmGetMfeStats, rras.mgmgetmfestats
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
 - MgmGetMfeStats
 - mgm/MgmGetMfeStats
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
 - MgmGetMfeStats
---

# MgmGetMfeStats function


## -description

The 
<b>MgmGetMfeStats</b> function retrieves the statistics for a specific MFE. The statistics returned include the packets received, bytes received, and the packets forwarded on each outgoing interface.

## -parameters

### -param pimm [in]

Pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a> structure that specifies the MFE for which to retrieve statistics. The information to be returned is indicated by the <b>dwSource</b> and <b>dwGroup</b> members of the 
<b>MIB_IPMCAST_MFE</b> structure.

### -param pdwBufferSize [in, out]

On input, <i>pdwBufferSize</i> is a pointer to a <b>DWORD</b>-sized memory location that contains the size, in bytes, of the buffer pointed to by <i>pbBuffer</i>. 




On output, if the return value is ERROR_INSUFFICIENT_BUFFER, <i>pdwBufferSize</i> receives the minimum size the buffer pointed to by <i>pbBuffer</i> must be to hold the set of MFE statistics; otherwise the value of <i>pdwBufferSize</i> remains unchanged.

### -param pbBuffer [in, out]

On input, the client must supply a pointer to a buffer. 




On output, <i>pbBuffer</i> contains the specified set of MFE statistics.

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
The specified buffer is too small for the statistics for even one MFE. The client should check the value of <i>pdwBufferSize</i> for the minimum buffer size required to retrieve statistics for one MFE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified MFE was not found.

</td>
</tr>
</table>

## -remarks

The MFE statistics are returned in either an <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a> or <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a> structure determined by the <i>dwFlags</i> parameter.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetfirstmfestats">MgmGetFirstMfeStats</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgetnextmfestats">MgmGetNextMfeStats</a>
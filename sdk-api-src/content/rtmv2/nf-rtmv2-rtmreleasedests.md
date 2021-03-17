---
UID: NF:rtmv2.RtmReleaseDests
title: RtmReleaseDests function (rtmv2.h)
description: The RtmReleaseDests function releases the destination handles.
helpviewer_keywords: ["RtmReleaseDests","RtmReleaseDests function [RAS]","_rtmv2ref_rtmreleasedests","rras.rtmreleasedests","rtmv2/RtmReleaseDests"]
old-location: rras\rtmreleasedests.htm
tech.root: RRAS
ms.assetid: eb338b7f-8461-4980-b92f-09d976661ff2
ms.date: 12/05/2018
ms.keywords: RtmReleaseDests, RtmReleaseDests function [RAS], _rtmv2ref_rtmreleasedests, rras.rtmreleasedests, rtmv2/RtmReleaseDests
req.header: rtmv2.h
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
 - RtmReleaseDests
 - rtmv2/RtmReleaseDests
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
 - RtmReleaseDests
---

# RtmReleaseDests function


## -description

The 
<b>RtmReleaseDests</b> function releases the destination handles.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NumDests [in]

Specifies the number of destinations in <i>DestInfos</i>.

### -param DestInfos [in]

Pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures to release. The destinations were obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>

## -remarks

Do not use this function to release 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures obtained from a call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>. Use 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a> instead.

The 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure is a variable-sized structure. If a destination contains information for more than one view, the size of 
<b>RTM_DEST_INFO</b> increases for each view. Use the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_size_of_dest_info">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>DestInfos</i> buffer to allocate before calling this function.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatedestenum">RtmCreateDestEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>
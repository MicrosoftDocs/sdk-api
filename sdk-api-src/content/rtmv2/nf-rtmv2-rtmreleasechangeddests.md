---
UID: NF:rtmv2.RtmReleaseChangedDests
title: RtmReleaseChangedDests function (rtmv2.h)
description: The RtmReleaseChangedDests function releases the changed destination handles.
helpviewer_keywords: ["RtmReleaseChangedDests","RtmReleaseChangedDests function [RAS]","_rtmv2ref_rtmreleasechangeddests","rras.rtmreleasechangeddests","rtmv2/RtmReleaseChangedDests"]
old-location: rras\rtmreleasechangeddests.htm
tech.root: RRAS
ms.assetid: 542cb23f-81c2-4b29-b049-ebb5827b1d62
ms.date: 12/05/2018
ms.keywords: RtmReleaseChangedDests, RtmReleaseChangedDests function [RAS], _rtmv2ref_rtmreleasechangeddests, rras.rtmreleasechangeddests, rtmv2/RtmReleaseChangedDests
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
 - RtmReleaseChangedDests
 - rtmv2/RtmReleaseChangedDests
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
 - RtmReleaseChangedDests
---

# RtmReleaseChangedDests function


## -description

The 
<b>RtmReleaseChangedDests</b> function releases the changed destination handles.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NotifyHandle [in]

Handle to a change notification, obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

### -param NumDests [in]

Specifies the number of destinations in <i>ChangedDests</i>.

### -param ChangedDests [in]

Pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures to release. The changed destinations were obtained from a prior call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

Always use this function to release changed 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures obtained from a call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.

The 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure is a variable-sized structure. If a destination contains information for more than one view, the size of 
<b>RTM_DEST_INFO</b> increases for each view. Use the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_size_of_dest_info">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>ChangedDests</i> buffer to allocate before calling this function.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangestatus">RtmGetChangeStatus</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmignorechangeddests">RtmIgnoreChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmismarkedforchangenotification">RtmIsMarkedForChangeNotification</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmmarkdestforchangenotification">RtmMarkDestForChangeNotification</a>
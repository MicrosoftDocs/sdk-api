---
UID: NF:rtmv2.RTM_SIZE_OF_DEST_INFO
title: RTM_SIZE_OF_DEST_INFO macro
author: windows-sdk-content
description: The RTM_SIZE_OF_DEST_INFO macro returns the size of the destination information structure (RTM_DEST_INFO).
old-location: rras\rtm_size_of_dest_info.htm
old-project: RRAS
ms.assetid: faad2b79-dcd0-47e7-95ab-05f6bad36650
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RTM_SIZE_OF_DEST_INFO, RTM_SIZE_OF_DEST_INFO macro [RAS], _rtmv2ref_rtm_size_of_dest_info, rras.rtm_size_of_dest_info, rtmv2/RTM_SIZE_OF_DEST_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_SIZE_OF_DEST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RTM_SIZE_OF_DEST_INFO macro


## -description


The 
<b>RTM_SIZE_OF_DEST_INFO</b> macro returns the size of the destination information structure (<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a>). The size of this structure is variable, and is based on the number of views for which it contains information. Use this macro when allocating memory for destination information.


## -parameters




### -param NumViews

Specifies the number of views in the destination structure.


## -remarks



If the client  only uses one view per destination, the client can allocate an 
<a href="https://msdn.microsoft.com/6712ed2f-c5b4-416b-b345-a3d0c5d26820">RTM_DEST_INFO</a> structure statically.

The macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define RTM_DEST_VIEW_INFO_SIZE                             \
    FIELD_OFFSET(RTM_DEST_INFO, ViewInfo)

#define RTM_SIZE_OF_DEST_INFO(NumViews)                     \
    (sizeof(RTM_DEST_INFO) - RTM_BASIC_DEST_INFO_SIZE)

#define RTM_BASIC_DEST_INFO_SIZE                            \
    (RTM_BASIC_DEST_INFO_SIZE + (NumViews) *                \
    RTM_DEST_VIEW_INFO_SIZE)
</pre>
</td>
</tr>
</table></span></div>



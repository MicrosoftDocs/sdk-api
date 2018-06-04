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



---
UID: NS:naptypes.tagFixupInfo
title: tagFixupInfo
author: windows-sdk-content
description: Contains fix-up information for the Sysytem Health Agent (SHA).
old-location: nap\fixupinfo_struct.htm
old-project: NAP
ms.assetid: 8f91534e-3281-4d5a-9af7-5f08eb0243f0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FixupInfo, FixupInfo structure [NAP], nap.fixupinfo_struct, naptypes/FixupInfo, tagFixupInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FixupInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	NapTypes.h
api_name:
-	FixupInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagFixupInfo structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FixupInfo</b> structure contains fix-up information for the Sysytem Health Agent (SHA).


## -struct-fields




### -field state

A <a href="https://msdn.microsoft.com/cde1f9df-f4d9-4601-a513-e00639ee9b6e">FixupState</a> value that defines the fix-up state of the SHA.


### -field percentage

A <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">Percentage</a> data type that contains the percentage of remediation that is complete. This member is a nonzero value between 0 (zero) and 100 when <b>state</b> is equal to <a href="https://msdn.microsoft.com/cde1f9df-f4d9-4601-a513-e00639ee9b6e">FixupStateInProgress</a>; otherwise, it is 0 (zero).

<div class="alert"><b>Note</b>  If the SHA does not support percentages, this value is either 0, which indicates the SHA update has not started; or 101, which indicates the SHA is in the process of updating.</div>
<div> </div>

### -field resultCodes

A <a href="https://msdn.microsoft.com/9d608f0a-9841-48e6-8856-2d8c1afc3e5d">ResultCodes</a> structure that contains the SHA defined HRESULT values returned to the NAP Agent in a call to <a href="https://msdn.microsoft.com/cf919b56-3d40-4c49-9c91-25c20ae5ccda">GetFixupInfo</a>.


### -field fixupMsgId

A <a href="https://msdn.microsoft.com/54f2866b-4333-4fc8-bb25-b7d4ae72b7dc">MessageID</a> value that contains the SHA defined resource ID of a fix-up status structure.


## -remarks



If your SHA remediation process supports the reporting of percentage values during update, <b>percentage</b> is used to communicate the current progress as an integer percentage value. When the remediation update is complete, <b>percentage</b> must be set to 100, and <b>state</b> must be set to <b>fixupStateSuccess</b>. If remediation is not complete, <b>percentage</b> must be set to a value between 0 and 99, inclusive, and <b>state</b> must be set to <b>fixupStateInProgress</b>.

If your remediation process does not support the reporting of percentage values, then as long as <b>state</b> is set to <b>fixupStateInProgress</b>, <b>percentage</b> must be set to a value of 101, which indicates the remediation process is in a general "updating" state but the amount of completion is unknown. When remediation completes, <b>state</b> must be set to <b>fixupStateSuccess</b> and <b>percentage</b> must be set to 100.

If the SHA cannot update the fix-up information, then <b>state</b> must be set to <b>fixupStateCouldNotUpdate</b>.




## -see-also




<a href="https://msdn.microsoft.com/cde1f9df-f4d9-4601-a513-e00639ee9b6e">FixupState</a>



<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>



<a href="https://msdn.microsoft.com/9d608f0a-9841-48e6-8856-2d8c1afc3e5d">ResultCodes</a>
 

 


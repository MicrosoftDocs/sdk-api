---
UID: NF:winsync.ICoreFragment.GetRangeCount
title: ICoreFragment::GetRangeCount
author: windows-sdk-content
description: Gets the number of ranges that are contained in this knowledge fragment.
old-location: winsync\icorefragment_getrangecount.htm
tech.root: winsync
ms.assetid: 8eb33224-f017-4f3b-bbf9-14d388d0868f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRangeCount, GetRangeCount method [Windows Sync], GetRangeCount method [Windows Sync],ICoreFragment interface, ICoreFragment interface [Windows Sync],GetRangeCount method, ICoreFragment.GetRangeCount, ICoreFragment::GetRangeCount, winsync.icorefragment_getrangecount, winsync/ICoreFragment::GetRangeCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ICoreFragment.GetRangeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- ICoreFragment.GetRangeCount
: 
---

# ICoreFragment::GetRangeCount


## -description


Gets the number of ranges that are contained in this knowledge fragment.


## -parameters




### -param pRangeCount [out]

Returns the number of ranges that are contained in this knowledge fragment.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



An <b>ICoreFragment</b> object contains one or more ranges. Each range specifies a set of item IDs and a clock vector that defines what is known about the items in the range.





## -see-also




<a href="https://msdn.microsoft.com/3e232531-ad44-4ad1-b186-46edbc07291b">ICoreFragment Interface</a>
 

 


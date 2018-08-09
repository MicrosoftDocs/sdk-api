---
UID: NF:winsync.IChangeUnitListFilterInfo.Initialize
title: IChangeUnitListFilterInfo::Initialize
author: windows-sdk-content
description: Initializes a new instance of the IChangeUnitListFilterInfo class that contains the specified array of change unit IDs.
old-location: winsync\ichangeunitlistfilterinfo_initialize.htm
old-project: winsync
ms.assetid: ee3f86dc-8f5a-4b9b-ac06-b836898392ba
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IChangeUnitListFilterInfo interface [Windows Sync],Initialize method, IChangeUnitListFilterInfo.Initialize, IChangeUnitListFilterInfo::Initialize, Initialize, Initialize method [Windows Sync], Initialize method [Windows Sync],IChangeUnitListFilterInfo interface, winsync.ichangeunitlistfilterinfo_initialize, winsync/IChangeUnitListFilterInfo::Initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeUnitListFilterInfo.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeUnitListFilterInfo::Initialize


## -description


Initializes a new instance of the <b>IChangeUnitListFilterInfo</b> class that contains the specified array of change unit IDs.


## -parameters




### -param ppbChangeUnitIds [in]

The array of change unit IDs that indicate which change units are included by this filter.


### -param dwChangeUnitCount [in]

The number of change unit IDs that are contained in <i>ppbChangeUnitIds</i>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwChangeUnitCount</i> is 0, or any ID that is contained in <i>ppbChangeUnitIds</i> is not valid.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
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



An <b>IChangeUnitListFilterInfo</b> object can be reused. Calling <b>Initialize</b> more than one time frees any previously contained array of change unit IDs and replaces it with the array that is specified by <i>ppbChangeUnitIds</i>.




## -see-also




<a href="https://msdn.microsoft.com/fd379fc6-22e5-4165-b4e6-480bc65cccb3">IChangeUnitListFilterInfo Interface</a>
 

 


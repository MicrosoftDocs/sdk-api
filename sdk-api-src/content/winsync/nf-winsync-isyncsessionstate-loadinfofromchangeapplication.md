---
UID: NF:winsync.ISyncSessionState.LoadInfoFromChangeApplication
title: ISyncSessionState::LoadInfoFromChangeApplication (winsync.h)
author: windows-sdk-content
description: Stores data for a serialized change applier.
old-location: winsync\isyncsessionstate_loadinfofromchangeapplication.htm
tech.root: winsync
ms.assetid: 72c7947b-0eee-4b75-aff6-f208bebac3f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncSessionState interface [Windows Sync],LoadInfoFromChangeApplication method, ISyncSessionState.LoadInfoFromChangeApplication, ISyncSessionState::LoadInfoFromChangeApplication, LoadInfoFromChangeApplication, LoadInfoFromChangeApplication method [Windows Sync], LoadInfoFromChangeApplication method [Windows Sync],ISyncSessionState interface, winsync.isyncsessionstate_loadinfofromchangeapplication, winsync/ISyncSessionState::LoadInfoFromChangeApplication
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
 - ISyncSessionState.LoadInfoFromChangeApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState::LoadInfoFromChangeApplication


## -description


Stores data for a serialized change applier.


## -parameters




### -param pbChangeApplierInfo [in]

The serialized change applier data.


### -param cbChangeApplierInfo [in]

Specifies the number of bytes in <i>pbChangeApplierInfo</i>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeApplierInfo</i> is not <b>NULL</b> and <i>cbChangeApplierInfo</i> is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_DESERIALIZATION</b></dt>
</dl>
</td>
<td width="60%">
The serialized data is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>
 

 


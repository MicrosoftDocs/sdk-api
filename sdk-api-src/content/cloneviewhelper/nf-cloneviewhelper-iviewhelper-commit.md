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

# IViewHelper::Commit


## -description


The <b>Commit</b> method invalidates a Video Present Network (VidPN) on all graphics adapters. 


## -parameters






## -returns



The <b>Commit</b> method returns one of the following values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
<b>Commit</b> successfully invalidated a VidPN. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any other error code (that is defined in <i>Winerror.h</i>) will cause TMM to not restore connections.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



After <b>Commit</b> succeeds, the sources and targets on all of the graphics adapters are set. 

TMM calls <b>Commit</b> whenever a set of operations must be applied. For example, TMM might call <b>Commit</b> after a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568174">IViewHelper::SetActiveTopology</a> method on a graphics adapter that requires for a source and targets to be mapped. TMM does not pass in the adapter name to <b>Commit</b> because the VidPN on all adapters should be invalidated. 

A call to <b>Commit</b> will no longer replace a call to <b>ChangeDisplaySettingsEx</b>(<b>NULL</b>, <b>NULL</b>, <b>NULL</b>, 0, <b>NULL</b>). However, TMM always ends its graphics operations with a <b>Commit</b> call. For more information about <b>ChangeDisplaySettingsEx</b>, see the Microsoft Windows SDK documentation. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568174">IViewHelper::SetActiveTopology</a>
 

 


---
UID: NF:tuner.ITuningSpaceContainer.FindID
title: ITuningSpaceContainer::FindID
author: windows-sdk-content
description: The FindID method retrieves the ID of a specified tuning space within the collection.
old-location: mstv\ituningspacecontainer_findid.htm
tech.root: mstv
ms.assetid: 99ac47b4-4adc-4e12-b465-4db8ae20ff6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindID, FindID method [Microsoft TV Technologies], FindID method [Microsoft TV Technologies],ITuningSpaceContainer interface, ITuningSpaceContainer interface [Microsoft TV Technologies],FindID method, ITuningSpaceContainer.FindID, ITuningSpaceContainer::FindID, ITuningSpaceContainerFindID, mstv.ituningspacecontainer_findid, tuner/ITuningSpaceContainer::FindID
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - ITuningSpaceContainer.FindID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpaceContainer::FindID


## -description



The <b>FindID</b> method retrieves the ID of a specified tuning space within the collection.




## -parameters




### -param TuningSpace [in]

Pointer to the <b>ITuningSpace</b> interface of the tuning space.


### -param ID [out]

Pointer to a variable that receives the ID of the tuning space. The returned value is specific to this collection object (which represents the local system).


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified tuning space is not a member of this collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 


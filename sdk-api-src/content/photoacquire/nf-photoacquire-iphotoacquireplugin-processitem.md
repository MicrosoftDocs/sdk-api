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

# IPhotoAcquirePlugin::ProcessItem


## -description



The <code>ProcessItem</code> method provides additional functionality each time an item is processed. The application provides the implementation of the <code>ProcessItem</code> method.




## -parameters




### -param dwAcquireStage [in]

Specifies a double word value indicating whether this method is being called before or after processing an item. Must be one of: PAPS_PRESAVE, PAPS_POSTSAVE, or PAPS_CLEANUP.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>PAPS_PRESAVE</td>
<td>Indicates that the method is being called before saving the acquired file. During PAPS_PRESAVE, <a href="https://msdn.microsoft.com/47ee6a23-5a0b-4f45-b278-9ebbeebf4fbb">pPhotoAcquireItem::GetProperty</a> should be used to retrieve metadata from the original file, while new metadata to be written to the file should be added to <i>pPropertyStore</i>.</td>
</tr>
<tr>
<td>PAPS_POSTSAVE</td>
<td>Indicates that the method is being called after saving the acquired file.</td>
</tr>
<tr>
<td>PAPS_CLEANUP</td>
<td>Indicates that the user has canceled the acquire operation and any work done by the plug-in should be cleaned up.</td>
</tr>
</table>
 


### -param pPhotoAcquireItem [in]

Pointer to an <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object for the item being processed.


### -param pOriginalItemStream [in]

Pointer to an <b>IStream</b> object for the original item. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_POSTSAVE.


### -param pszFinalFilename [in]

The file name of the destination of the item. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_PRESAVE.


### -param pPropertyStore [in]

The item's property store. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_POSTSAVE.


## -returns



The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c8a0a49-8c15-4db2-8231-a48a3f76eb62">IPhotoAcquirePlugin Interface</a>
 

 


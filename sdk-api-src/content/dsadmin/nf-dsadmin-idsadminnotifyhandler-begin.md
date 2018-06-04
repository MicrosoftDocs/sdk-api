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

# IDsAdminNotifyHandler::Begin


## -description


The <b>IDsAdminNotifyHandler::Begin</b> method is called when an event that  the notification handler has requested is occurring. The notification handler specifies the events to receive notifications for when <a href="https://msdn.microsoft.com/7fcd49d3-ccdb-4d55-96ea-cc925a36c366">IDsAdminNotifyHandler::Initialize</a> is called.


## -parameters




### -param uEvent [in]

Contains a value the specifies the type of event that is occurring. This can be one of the following values.



#### DSA_NOTIFY_DEL

An object is deleted.



#### DSA_NOTIFY_REN

An object is renamed.



#### DSA_NOTIFY_MOV

An object is moved to another container.



#### DSA_NOTIFY_PROP

One or more properties of an object is  modified.


### -param pArg1 [in]

Pointer to an <a href="_ole_idataobject">IDataObject</a> interface that supports the <a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a> clipboard format. The contents of the data object will vary depending on  the value of <i>uEvent</i>. For more information, see the Remarks section.


### -param pArg2 [in]

Pointer to an <a href="_ole_idataobject">IDataObject</a> interface that supports the <a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a> clipboard format. The value of this parameter and the contents of the data object will vary depending on the value of <i>uEvent</i>. For more information, see the Remarks section.


### -param puFlags [out]

Pointer to a <b>ULONG</b> value that receives a set of flags that modify the behavior of the notification handler in the notification confirmation dialog box. This can be zero or a combination of one or more of the following values.



#### DSA_NOTIFY_FLAG_ADDITIONAL_DATA

If this flag is set, the entry for this notification handler in the confirmation dialog box is selected. If this flag is not set, the entry for this notification handler in the confirmation dialog box is not selected.



#### DSA_NOTIFY_FLAG_FORCE_ADDITIONAL_DATA

If this flag is set, the entry  for this notification handler in the confirmation dialog box is disabled and the user cannot change the selection state.


### -param pBstr [out]

Pointer to a <b>BSTR</b> that receives a string that contains  the name and/or description of the notification handler. This string  is displayed in the confirmation dialog box. This string must be allocated by calling the <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> function. The caller must free this string when it is no longer required. If this parameter receives <b>NULL</b> or an empty string, the notification handler is not added to the confirmation dialog box and <a href="https://msdn.microsoft.com/ac0b9da5-b0e3-4280-ae9c-602e28c907b1">IDsAdminNotifyHandler::Notify</a> is not called.


## -returns



If the method succeeds, 
      <b>S_OK</b> is returned. If the method fails, a standard <b>HRESULT</b> value is returned.




## -remarks



The value and contents of <i>pArg1</i> and <i>pArg2</i> vary depending upon the event processed as indicated by <i>uEvent</i>. The following list explains what <i>pArg1</i> and <i>pArg2</i> will contain for each different event type.

<table>
<tr>
<th><i>uEvent</i></th>
<th><i>pArg1</i></th>
<th><i>pArg2</i></th>
</tr>
<tr>
<td><b>DSA_NOTIFY_DEL</b></td>
<td>Contains the object deleted.</td>
<td>Not used. This will be <b>NULL</b>.</td>
</tr>
<tr>
<td><b>DSA_NOTIFY_REN</b></td>
<td>Contains the previous name of the object.</td>
<td>Contains the new name of the object.</td>
</tr>
<tr>
<td><b>DSA_NOTIFY_MOV</b></td>
<td>Contains the container that the object is moved from.</td>
<td>Contains the container that the object is moved to.</td>
</tr>
<tr>
<td><b>DSA_NOTIFY_PROP</b></td>
<td>Contains the object for which the properties have changed.</td>
<td>Not used. This will be <b>NULL</b>.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a>



<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>



<a href="https://msdn.microsoft.com/7fcd49d3-ccdb-4d55-96ea-cc925a36c366">IDsAdminNotifyHandler::Initialize</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>
 

 


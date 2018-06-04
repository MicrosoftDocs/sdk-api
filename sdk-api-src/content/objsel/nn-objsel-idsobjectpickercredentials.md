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

# IDsObjectPickerCredentials interface


## -description


The <b>IDsObjectPickerCredentials</b> interface 
    allows you to override credentials for the <a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a> 
    object implementing this interface.

To obtain an instance of this interface, call 
    <a href="_com_iunknown_queryinterface">QueryInterface</a> with the 
    <b>IID_IDsObjectPickerCredentials</b> interface identifier as shown below.


## -members

The <b>IDsObjectPickerCredentials</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb1c366d-10df-4e4f-a381-3f085bd136e2">SetCredentials</a>
</td>
<td align="left" width="63%">
Sets credentials to be used by the Object Picker.

</td>
</tr>
</table>Sets credentials to be used by the Object Picker.

 


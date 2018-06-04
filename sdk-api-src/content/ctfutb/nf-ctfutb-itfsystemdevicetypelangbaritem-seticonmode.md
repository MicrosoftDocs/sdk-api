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

# ITfSystemDeviceTypeLangBarItem::SetIconMode


## -description




## -parameters




### -param dwFlags [in]

Specifies how the system language bar item should display the icon. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The system language bar item should display a default icon for the item.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_DTLBI_USEPROFILEICON"></a><a id="tf_dtlbi_useprofileicon"></a><dl>
<dt><b>TF_DTLBI_USEPROFILEICON</b></dt>
</dl>
</td>
<td width="60%">
The system language bar item should display the icon specified for the language profile.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The system language bar item does not support this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0dc32f10-eecd-4203-992c-80eb0f991615">ITfSystemDeviceTypeLangBarItem</a>



<a href="https://msdn.microsoft.com/c1740636-7ba3-4748-9005-ee94d04dbb15">Miscellaneous Language Bar Constants</a>
 

 


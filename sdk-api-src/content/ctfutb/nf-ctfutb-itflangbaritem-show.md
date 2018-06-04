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

# ITfLangBarItem::Show


## -description




## -parameters




### -param fShow [in]

Contains a <b>BOOL</b> that indicates if the item should be shown or hidden. Contains a nonzero value if the item should be shown or zero otherwise.


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
The language bar item does not support this method.

</td>
</tr>
</table>
 




## -remarks



The language bar item implementation should update its visible status by modifying the value returned from <a href="https://msdn.microsoft.com/2f850553-ec79-4e2f-a4d5-c40dbaca0f01">ITfLangBarItem::GetStatus</a> to include or exclude the TF_LBI_STATUS_HIDDEN status flag. The implementation then prompts language bar to obtain the new status value by calling <a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_STATUS.

This method is only useful when the item has the TF_LBI_STYLE_HIDDENSTATUSCONTROL style. Without this style, only the language bar can show or hide the item.




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/2f850553-ec79-4e2f-a4d5-c40dbaca0f01">ITfLangBarItem::GetStatus
      </a>



<a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">
        ITfLangBarItemSink::OnUpdate
      </a>
 

 


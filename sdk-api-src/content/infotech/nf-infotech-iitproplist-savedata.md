---
UID: NF:infotech.IITPropList.SaveData
title: IITPropList::SaveData
author: windows-sdk-content
description: Saves the data size and data from the property list to a buffer.
old-location: htmlhelp\iitproplist_savedata.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsavedata.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SaveData method, IITPropList.SaveData, IITPropList::SaveData, SaveData, SaveData method [HTML Help Workshop], SaveData method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_savedata, infotech/IITPropList::SaveData, refIITPropListSaveData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: infotech.h
req.include-header: 
req.target-type: Windows
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
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITPropList.SaveData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITPropList::SaveData


## -description


Saves the data size and data from the property list to a buffer.




## -parameters




### -param lpvHeader [in]

Pointer to a buffer containing the header.




### -param dwHdrSize [in]

Size of the buffer containing the header.




### -param lpvData [out]

Pointer to a buffer to fill.




### -param dwBufSize [in]

Size of the buffer to fill.




## -returns



This method can return one of these values.

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
The property list was successfully saved.



</td>
</tr>
</table>
 




## -remarks



Make sure to pass a buffer large enough to hold the property list. Use <a href="https://msdn.microsoft.com/83d9fa7b-d814-4293-93b9-9454c01c1503">IITPropList::GetDataSize</a> to determine the buffer size to pass.






## -see-also




<a href="https://msdn.microsoft.com/09200749-bd1d-4266-895e-29e21525bac2">IITPropList</a>
 

 


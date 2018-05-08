---
UID: NF:infotech.IITPropList.SaveHeader
title: IITPropList::SaveHeader
author: windows-driver-content
description: Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.
old-location: htmlhelp\iitproplist_saveheader.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsaveheader.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SaveHeader method, IITPropList.SaveHeader, IITPropList::SaveHeader, SaveHeader, SaveHeader method [HTML Help Workshop], SaveHeader method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_saveheader, infotech/IITPropList::SaveHeader, refIITPropListSaveHeader
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IITPropList.SaveHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITPropList::SaveHeader


## -description


Saves the property ID and data type from the property list to a buffer. Only saves properties marked with a persistence state of TRUE.


## -parameters




### -param lpvData [out]

Pointer to a buffer to fill.




### -param dwHdrSize [in]

Size of the buffer.




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



Make sure to pass a buffer large enough to hold the property list. Use <a href="https://msdn.microsoft.com/73206149-cbc3-475d-8dc8-bb7547f41173">IITPropList::GetHeaderSize</a> to determine the buffer size to pass.






## -see-also




<a href="https://msdn.microsoft.com/09200749-bd1d-4266-895e-29e21525bac2">IITPropList</a>
 

 


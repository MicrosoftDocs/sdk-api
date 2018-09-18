---
UID: NF:oleidl.IViewObject.Unfreeze
title: IViewObject::Unfreeze
author: windows-sdk-content
description: Releases a drawing that was previously frozen using IViewObject::Freeze. The most common use of this method is for banded printing.
old-location: com\iviewobject_unfreeze.htm
tech.root: com
ms.assetid: 76f3c5f6-3f29-4a89-94e2-f77489e6a744
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IViewObject interface [COM],Unfreeze method, IViewObject.Unfreeze, IViewObject::Unfreeze, Unfreeze, Unfreeze method [COM], Unfreeze method [COM],IViewObject interface, _ole_iviewobject_unfreeze, com.iviewobject_unfreeze, oleidl/IViewObject::Unfreeze
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IViewObject.Unfreeze
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IViewObject::Unfreeze


## -description


Releases a drawing that was previously frozen using <a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a>. The most common use of this method is for banded printing.


## -parameters




### -param dwFreeze [in]

Contains a key previously returned from <a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a> that determines which view object to unfreeze.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Error in the unfreezing process or the object is currently not frozen.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a>
 

 


---
UID: NF:winsync.ISingleItemException.GetItemId
title: ISingleItemException::GetItemId method
author: windows-driver-content
description: Gets the ID of the item that is specified in the exception.
old-location: winsync\isingleitemexception_getitemid.htm
old-project: winsync
ms.assetid: 1bcea395-d383-434f-b3a6-cffd4419fce3
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetItemId method [Windows Sync], GetItemId method [Windows Sync], ISingleItemException interface, GetItemId,ISingleItemException.GetItemId, ISingleItemException, ISingleItemException interface [Windows Sync], GetItemId method, ISingleItemException::GetItemId, winsync.isingleitemexception_getitemid, winsync/ISingleItemException::GetItemId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISingleItemException.GetItemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISingleItemException::GetItemId method


## -description


Gets the ID of the item that is specified in the exception.


## -parameters




### -param pbItemId [in, out]

Returns the ID of the item that is specified in the exception.


### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbItemId</i>. Returns the number of bytes required to retrieve the ID when <i>pbItemId</i> is too small, or returns the number of bytes written.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbItemId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/623553cb-9dc2-4504-9c49-357a0526b130">ISingleItemException Interface</a>
 

 


---
UID: NF:recapis.DestroyWordList
title: DestroyWordList function
author: windows-sdk-content
description: Destroys the current word list.
old-location: tablet\destroywordlist.htm
tech.root: tablet
ms.assetid: 380e81a0-1df1-48b8-a582-a52badfc9ca6
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 380e81a0-1df1-48b8-a582-a52badfc9ca6, DestroyWordList, DestroyWordList function [Tablet PC], recapis/DestroyWordList, tablet.destroywordlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - DestroyWordList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyWordList function


## -description



Destroys the current word list.




## -parameters




### -param hwl

Handle to the word list.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the word list is incorrect.

</td>
</tr>
</table>
 




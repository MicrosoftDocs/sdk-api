---
UID: NF:photoacquire.IUserInputString.GetMruEntryAt
title: IUserInputString::GetMruEntryAt
author: windows-driver-content
description: The GetMruEntryAt method retrieves the entry at the given index in the most recently used list.
old-location: picacq\iuserinputstring_getmruentryat.htm
old-project: acquisition
ms.assetid: d03c3eba-e55c-421d-acfa-fea6aa645cc5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetMruEntryAt, GetMruEntryAt method [Picture Acquisition], GetMruEntryAt method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetMruEntryAt method, IUserInputString.GetMruEntryAt, IUserInputString::GetMruEntryAt, IUserInputStringGetMruEntryAt, photoacquire/IUserInputString::GetMruEntryAt, picacq.iuserinputstring_getmruentryat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: photoacquire.h
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IUserInputString.GetMruEntryAt
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IUserInputString::GetMruEntryAt


## -description



The <code>GetMruEntryAt</code> method retrieves the entry at the given index in the most recently used list.




## -parameters




### -param nIndex [in]

Integer containing the index at which to retrieve the entry.


### -param pbstrMruEntry [out]

Pointer to a string containing the most recently used entry.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f942fefc-2db1-4067-8311-f9ebbaca9d31">IUserInputString Interface</a>
 

 


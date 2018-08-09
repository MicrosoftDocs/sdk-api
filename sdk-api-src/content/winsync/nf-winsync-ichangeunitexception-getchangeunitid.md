---
UID: NF:winsync.IChangeUnitException.GetChangeUnitId
title: IChangeUnitException::GetChangeUnitId
author: windows-sdk-content
description: Gets the change unit ID for the change unit that is associated with the exception.
old-location: winsync\ichangeunitexception_getchangeunitid.htm
old-project: winsync
ms.assetid: 25a6eed2-6851-4a24-afd2-91982dc2bb8e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetChangeUnitId, GetChangeUnitId method [Windows Sync], GetChangeUnitId method [Windows Sync],IChangeUnitException interface, IChangeUnitException interface [Windows Sync],GetChangeUnitId method, IChangeUnitException.GetChangeUnitId, IChangeUnitException::GetChangeUnitId, winsync.ichangeunitexception_getchangeunitid, winsync/IChangeUnitException::GetChangeUnitId
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeUnitException.GetChangeUnitId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeUnitException::GetChangeUnitId


## -description


Gets the change unit ID for the change unit that is associated with the exception.


## -parameters




### -param pbChangeUnitId [in, out]

Returns the change unit ID that is associated with the exception.


### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbChangeUnitId</i>. Returns the number of bytes required to retrieve the ID when <i>pbChangeUnitId</i> is too small, or the number of bytes written.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3b47abab-0a33-405f-a765-307ab800bad6">IChangeUnitException Interface</a>
 

 


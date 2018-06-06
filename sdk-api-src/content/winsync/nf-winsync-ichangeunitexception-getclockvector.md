---
UID: NF:winsync.IChangeUnitException.GetClockVector
title: IChangeUnitException::GetClockVector
author: windows-sdk-content
description: Gets the clock vector that is associated with this exception.
old-location: winsync\ichangeunitexception_getclockvector.htm
old-project: winsync
ms.assetid: 1cf95acf-23ab-49c8-bd63-7aff9bad8f25
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetClockVector, GetClockVector method [Windows Sync], GetClockVector method [Windows Sync],IChangeUnitException interface, IChangeUnitException interface [Windows Sync],GetClockVector method, IChangeUnitException.GetClockVector, IChangeUnitException::GetClockVector, winsync.ichangeunitexception_getclockvector, winsync/IChangeUnitException::GetClockVector
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
 - IChangeUnitException.GetClockVector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeUnitException::GetClockVector


## -description


Gets the clock vector that is associated with this exception.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumClockVector</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that represents the clock vector that is associated with this exception.


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
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3b47abab-0a33-405f-a765-307ab800bad6">IChangeUnitException Interface</a>



<a href="https://msdn.microsoft.com/cf191502-dc51-44a7-a82f-a0e38537574f">IEnumClockVector Interface</a>
 

 


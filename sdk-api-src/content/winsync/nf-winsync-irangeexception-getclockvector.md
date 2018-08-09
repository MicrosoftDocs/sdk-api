---
UID: NF:winsync.IRangeException.GetClockVector
title: IRangeException::GetClockVector
author: windows-sdk-content
description: Gets the clock vector that is associated with this exception.
old-location: winsync\irangeexception_getclockvector.htm
old-project: winsync
ms.assetid: 9a13bb4c-ed0e-45f0-a78f-13eadd32760e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetClockVector, GetClockVector method [Windows Sync], GetClockVector method [Windows Sync],IRangeException interface, IRangeException interface [Windows Sync],GetClockVector method, IRangeException.GetClockVector, IRangeException::GetClockVector, winsync.irangeexception_getclockvector, winsync/IRangeException::GetClockVector
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
 - IRangeException.GetClockVector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IRangeException::GetClockVector


## -description


Gets the clock vector that is associated with this exception.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumClockVector</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and represents the clock vector that is associated with this exception.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7eea9fe0-80e7-43a9-a797-df12d4d809dc">IRangeException Interface</a>
 

 


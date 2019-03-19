---
UID: NF:msctf.ITfThreadMgr2.GetGlobalCompartment
title: ITfThreadMgr2::GetGlobalCompartment (msctf.h)
author: windows-sdk-content
description: Obtains the global compartment manager object.
old-location: tsf\itfthreadmgr2_getglobalcompartment.htm
tech.root: TSF
ms.assetid: AC1D27C5-C9D9-4658-AC3C-9C3A723F8597
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGlobalCompartment, GetGlobalCompartment method [Text Services Framework], GetGlobalCompartment method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],GetGlobalCompartment method, ITfThreadMgr2.GetGlobalCompartment, ITfThreadMgr2::GetGlobalCompartment, msctf/ITfThreadMgr2::GetGlobalCompartment, tsf.itfthreadmgr2_getglobalcompartment
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - msctf.h
api_name:
 - ITfThreadMgr2.GetGlobalCompartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfThreadMgr2::GetGlobalCompartment


## -description


Obtains the global compartment manager object.


## -parameters




### -param ppCompMgr [out]

Pointer to a <a href="https://msdn.microsoft.com/7cdc5c82-4aac-4ec9-b791-93cea33ba8d2">ITfCompartmentMgr</a> interface that receives the global compartment manager.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppCompMgr</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 


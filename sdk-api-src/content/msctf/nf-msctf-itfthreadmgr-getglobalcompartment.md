---
UID: NF:msctf.ITfThreadMgr.GetGlobalCompartment
title: ITfThreadMgr::GetGlobalCompartment
author: windows-driver-content
description: ITfThreadMgr::GetGlobalCompartment method
old-location: tsf\itfthreadmgr_getglobalcompartment.htm
old-project: TSF
ms.assetid: 801e2c3a-0445-4630-83ba-55f51ef2704e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetGlobalCompartment, GetGlobalCompartment method [Text Services Framework], GetGlobalCompartment method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],GetGlobalCompartment method, ITfThreadMgr.GetGlobalCompartment, ITfThreadMgr::GetGlobalCompartment, _tsf_itfthreadmgr_getglobalcompartment_ref, msctf/ITfThreadMgr::GetGlobalCompartment, tsf.itfthreadmgr_getglobalcompartment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfThreadMgr.GetGlobalCompartment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr::GetGlobalCompartment


## -description




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




<a href="https://msdn.microsoft.com/7cdc5c82-4aac-4ec9-b791-93cea33ba8d2">ITfCompartmentMgr
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>
 

 


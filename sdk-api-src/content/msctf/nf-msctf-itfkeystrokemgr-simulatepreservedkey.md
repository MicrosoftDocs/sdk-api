---
UID: NF:msctf.ITfKeystrokeMgr.SimulatePreservedKey
title: ITfKeystrokeMgr::SimulatePreservedKey
author: windows-driver-content
description: ITfKeystrokeMgr::SimulatePreservedKey method
old-location: tsf\itfkeystrokemgr_simulatepreservedkey.htm
old-project: TSF
ms.assetid: 09ad2203-a254-4afd-bdee-b8c51daa6e95
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],SimulatePreservedKey method, ITfKeystrokeMgr.SimulatePreservedKey, ITfKeystrokeMgr::SimulatePreservedKey, SimulatePreservedKey, SimulatePreservedKey method [Text Services Framework], SimulatePreservedKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_simulatepreservedkey_ref, msctf/ITfKeystrokeMgr::SimulatePreservedKey, tsf.itfkeystrokemgr_simulatepreservedkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	ITfKeystrokeMgr.SimulatePreservedKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeystrokeMgr::SimulatePreservedKey


## -description




## -parameters




### -param pic [in]

Pointer to the application context. This value was returned by a previous call to <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a>.


### -param rguid [in]

Contains the command GUID of the preserved key.


### -param pfEaten [out]

Pointer to a BOOL that indicates if the key event was handled. If this value receives <b>TRUE</b>, the key event was handled. If this value is <b>FALSE</b>, the key event was not handled.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The preserved key cannot be simulated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/93c1591d-2c95-45cb-8fc5-5726e905f202">ITfKeystrokeMgr</a>
 

 


---
UID: NF:msctf.ITfCompartmentMgr.ClearCompartment
title: ITfCompartmentMgr::ClearCompartment
author: windows-driver-content
description: ITfCompartmentMgr::ClearCompartment method
old-location: tsf\itfcompartmentmgr_clearcompartment.htm
old-project: TSF
ms.assetid: 862ec077-b192-412a-b80c-6105f503ed21
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ClearCompartment, ClearCompartment method [Text Services Framework], ClearCompartment method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],ClearCompartment method, ITfCompartmentMgr.ClearCompartment, ITfCompartmentMgr::ClearCompartment, _tsf_itfcompartmentmgr_clearcompartment_ref, msctf/ITfCompartmentMgr::ClearCompartment, tsf.itfcompartmentmgr_clearcompartment
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
-	ITfCompartmentMgr.ClearCompartment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompartmentMgr::ClearCompartment


## -description




## -parameters




### -param tid [in]

Contains a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that identifies the client.


### -param rguid [in]

Contains a GUID that identifies the compartment.


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
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The compartment cannot be found.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The owner must clear this compartment.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7cdc5c82-4aac-4ec9-b791-93cea33ba8d2">ITfCompartmentMgr</a>



<a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId
      </a>
 

 


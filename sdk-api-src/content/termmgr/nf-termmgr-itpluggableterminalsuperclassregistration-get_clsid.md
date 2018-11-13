---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.get_CLSID
title: ITPluggableTerminalSuperclassRegistration::get_CLSID
author: windows-sdk-content
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal.
old-location: tapi3\itpluggableterminalsuperclassregistration_get_clsid.htm
tech.root: tapi
ms.assetid: d343284c-ffe1-4491-8476-37bcdd6e1a97
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalSuperclassRegistration.get_CLSID, ITPluggableTerminalSuperclassRegistration::get_CLSID, _tapi3_itpluggableterminalsuperclassregistration_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_get_clsid, termmgr/ITPluggableTerminalSuperclassRegistration::get_CLSID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassRegistration.get_CLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalSuperclassRegistration::get_CLSID


## -description


The 
<b>get_CLSID</b> method gets the CLSID used to <b>CoCreateInstance</b> the terminal.


## -parameters




### -param pCLSID [out]

 The <b>BSTR</b> representation of the CLSID. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCLSID</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>



<a href="https://msdn.microsoft.com/ccb7159d-e838-408b-9565-a9854c4ba592">put_CLSID</a>
 

 


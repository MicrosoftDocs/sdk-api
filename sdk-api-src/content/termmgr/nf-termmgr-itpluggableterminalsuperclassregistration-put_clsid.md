---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.put_CLSID
title: ITPluggableTerminalSuperclassRegistration::put_CLSID
author: windows-driver-content
description: The put_CLSID method sets the CLSID used to CoCreateInstance the terminal.
old-location: tapi3\itpluggableterminalsuperclassregistration_put_clsid.htm
old-project: Tapi
ms.assetid: ccb7159d-e838-408b-9565-a9854c4ba592
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],put_CLSID method, ITPluggableTerminalSuperclassRegistration.put_CLSID, ITPluggableTerminalSuperclassRegistration::put_CLSID, _tapi3_itpluggableterminalsuperclassregistration_put_clsid, put_CLSID, put_CLSID method [TAPI 2.2], put_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_put_clsid, termmgr/ITPluggableTerminalSuperclassRegistration::put_CLSID
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPluggableTerminalSuperclassRegistration.put_CLSID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalSuperclassRegistration::put_CLSID


## -description


The 
<b>put_CLSID</b> method sets the CLSID used to <b>CoCreateInstance</b> the terminal.


## -parameters




### -param bstrCLSID [in]

The <b>BSTR</b> representation of the CLSID.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>bstrCLSID</i> parameter is not valid.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>



<a href="https://msdn.microsoft.com/d343284c-ffe1-4491-8476-37bcdd6e1a97">get_CLSID</a>
 

 


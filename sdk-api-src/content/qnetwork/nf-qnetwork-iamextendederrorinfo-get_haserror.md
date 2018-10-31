---
UID: NF:qnetwork.IAMExtendedErrorInfo.get_HasError
title: IAMExtendedErrorInfo::get_HasError
author: windows-sdk-content
description: The get_HasError method queries whether an error occurred.
old-location: dshow\iamextendederrorinfo_get_haserror.htm
tech.root: DirectShow
ms.assetid: 8aad2849-5a99-484a-8830-e014672e62fb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAMExtendedErrorInfo interface [DirectShow],get_HasError method, IAMExtendedErrorInfo.get_HasError, IAMExtendedErrorInfo::get_HasError, IAMExtendedErrorInfoget_HasError, dshow.iamextendederrorinfo_get_haserror, get_HasError, get_HasError method [DirectShow], get_HasError method [DirectShow],IAMExtendedErrorInfo interface, qnetwork/IAMExtendedErrorInfo::get_HasError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Qnetwork.h
api_name:
 - IAMExtendedErrorInfo.get_HasError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtendedErrorInfo::get_HasError


## -description



The <code>get_HasError</code> method queries whether an error occurred.




## -parameters




### -param pHasError

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>No error.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>An error occurred.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



If <i>pHasError</i> is true, you can call the <b>get_ErrorCode</b> and <b>get_ErrorDescription</b> methods to determine the nature of the error.




## -see-also




<a href="https://msdn.microsoft.com/0e3274e6-7c22-4175-8b2e-cdf4afc1225e">IAMExtendedErrorInfo Interface</a>
 

 


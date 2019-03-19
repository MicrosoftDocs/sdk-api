---
UID: NF:wsdbase.IWSDHttpAddress.SetPath
title: IWSDHttpAddress::SetPath (wsdbase.h)
author: windows-sdk-content
description: Sets the URI path for this address.
old-location: ncd\iwsdhttpaddress_setpath.htm
tech.root: WsdApi
ms.assetid: 4bad84a6-f321-4275-9787-f6bae83c807e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDHttpAddress interface,SetPath method, IWSDHttpAddress.SetPath, IWSDHttpAddress::SetPath, SetPath, SetPath method, SetPath method,IWSDHttpAddress interface, ncd.iwsdhttpaddress_setpath, wsdbase/IWSDHttpAddress::SetPath
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpAddress.SetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDHttpAddress::SetPath


## -description


Sets the URI path for this address.


## -parameters




### -param pszPath [in]

The URI path to use for this address.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszPath</i> exceeds WSD_MAX_TEXT_LENGTH (8192). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a>
 

 


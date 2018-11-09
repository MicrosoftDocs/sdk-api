---
UID: NF:wmcodecdsp.IWMResamplerProps.SetHalfFilterLength
title: IWMResamplerProps::SetHalfFilterLength
author: windows-sdk-content
description: Specifies the quality of the output.
old-location: mf\iwmresamplerpropssethalffilterlength.htm
tech.root: medfound
ms.assetid: ac35fafa-d1f1-4470-b4e3-0e6fce792a11
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IWMResamplerProps interface [Media Foundation],SetHalfFilterLength method, IWMResamplerProps.SetHalfFilterLength, IWMResamplerProps::SetHalfFilterLength, SetHalfFilterLength, SetHalfFilterLength method [Media Foundation], SetHalfFilterLength method [Media Foundation],IWMResamplerProps interface, codecapi.iwmresamplerpropssethalffilterlength, mf.iwmresamplerpropssethalffilterlength, wmcodecdsp/IWMResamplerProps::SetHalfFilterLength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmcodecdsp.h
api_name:
 - IWMResamplerProps.SetHalfFilterLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMResamplerProps::SetHalfFilterLength


## -description


Specifies the quality of the output. 



## -parameters




### -param lhalfFilterLen [in]

Specifies the quality of the output. The valid range is 1 to 60, inclusive.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



This method is equivalent to setting the <a href="https://msdn.microsoft.com/7b45633b-7f1c-4951-a462-ad6240b9ca31">MFPKEY_WMRESAMP_FILTERQUALITY</a> property.




## -see-also




<a href="https://msdn.microsoft.com/af3cec68-59a2-4b9d-a279-e5af46e9c38e">IWMResamplerProps Interface</a>
 

 


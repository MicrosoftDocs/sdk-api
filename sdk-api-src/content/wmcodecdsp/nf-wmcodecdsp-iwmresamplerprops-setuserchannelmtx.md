---
UID: NF:wmcodecdsp.IWMResamplerProps.SetUserChannelMtx
title: IWMResamplerProps::SetUserChannelMtx method
author: windows-driver-content
description: Specifies the channel matrix.
old-location: mf\iwmresamplerpropssetuserchannelmtx.htm
old-project: medfound
ms.assetid: d7f225a9-c63d-4b4e-b75a-ed6156e594a0
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IWMResamplerProps, IWMResamplerProps interface [Media Foundation], SetUserChannelMtx method, IWMResamplerProps::SetUserChannelMtx, SetUserChannelMtx method [Media Foundation], SetUserChannelMtx method [Media Foundation], IWMResamplerProps interface, SetUserChannelMtx,IWMResamplerProps.SetUserChannelMtx, codecapi.iwmresamplerpropssetuserchannelmtx, mf.iwmresamplerpropssetuserchannelmtx, wmcodecdsp/ IWMResamplerProps::SetUserChannelMtx
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
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmcodecdsp.h
api_name:
-	IWMResamplerProps.SetUserChannelMtx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMResamplerProps::SetUserChannelMtx method


## -description



Specifies the channel matrix.



## -parameters




### -param userChannelMtx [in]

Pointer to an array of floating-point values that represents a channel conversion matrix.


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



This method is equivalent to setting the <a href="https://msdn.microsoft.com/2f2a82bd-f051-4b05-a9c8-37aa4403fab4">MFPKEY_WMRESAMP_CHANNELMTX</a> property, except that the matrix is represented differently:

<ul>
<li>Values are floating point.</li>
<li>The matrix is transposed.</li>
</ul>
To convert from the integer values given in the MFPKEY_WMRESAMP_CHANNELMTX property to floating-point values, use the following formula:

<code>(float)pow(10.0,((double)Coeff)/(65536.0*20.0))</code>

where <i>Coeff</i> is an integer coefficient.




## -see-also




<a href="https://msdn.microsoft.com/af3cec68-59a2-4b9d-a279-e5af46e9c38e">IWMResamplerProps Interface</a>
 

 


---
UID: NF:wsdbase.IWSDSignatureProperty.IsMessageSignatureTrusted
title: IWSDSignatureProperty::IsMessageSignatureTrusted
author: windows-sdk-content
description: Specifies if a message signature is trusted.
old-location: ncd\iwsdsignatureproperty_ismessagesignaturetrusted.htm
tech.root: WsdApi
ms.assetid: b71ddd44-4823-455c-aea7-ee2f63b423bb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDSignatureProperty interface,IsMessageSignatureTrusted method, IWSDSignatureProperty.IsMessageSignatureTrusted, IWSDSignatureProperty::IsMessageSignatureTrusted, IsMessageSignatureTrusted, IsMessageSignatureTrusted method, IsMessageSignatureTrusted method,IWSDSignatureProperty interface, ncd.iwsdsignatureproperty_ismessagesignaturetrusted, wsdbase/IWSDSignatureProperty::IsMessageSignatureTrusted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - wsdapi.dll
api_name:
 - IWSDSignatureProperty.IsMessageSignatureTrusted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDSignatureProperty::IsMessageSignatureTrusted


## -description


Specifies if a message signature is trusted.


## -parameters




### -param pbSignatureTrusted [out]

A pointer to a boolean that specifies if a message signature is trusted.


## -returns



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
Method succeeded.

</td>
</tr>
</table>
 




## -remarks



A message is trusted if the signing certificate is among one of the certificates or in the certificate store passed down by the calling application in the <a href="https://msdn.microsoft.com/dc757897-032c-4ea3-8f4e-cf00d4ec385b">WSDCreateDiscoveryProvider2</a> call.




## -see-also




<a href="https://msdn.microsoft.com/10e95100-4890-4c00-b231-bb7125fed197">IWSDSignatureProperty</a>
 

 


---
UID: NF:wsdbase.IWSDSignatureProperty.IsMessageSigned
title: IWSDSignatureProperty::IsMessageSigned
author: windows-driver-content
description: Specifies if a message is signed.
old-location: ncd\iwsdsignatureproperty_ismessagesigned.htm
old-project: WsdApi
ms.assetid: ca91bb1e-b8a6-4cfe-850c-887b39ae239e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDSignatureProperty interface,IsMessageSigned method, IWSDSignatureProperty.IsMessageSigned, IWSDSignatureProperty::IsMessageSigned, IsMessageSigned, IsMessageSigned method, IsMessageSigned method,IWSDSignatureProperty interface, ncd.iwsdsignatureproperty_ismessagesigned, wsdbase/IWSDSignatureProperty::IsMessageSigned
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wsdapi.dll
api_name:
-	IWSDSignatureProperty.IsMessageSigned
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDSignatureProperty::IsMessageSigned


## -description


Specifies if a message is signed.


## -parameters




### -param pbSigned [out]

A pointer to a boolean that specifies if a message signature is signed.


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
 




## -see-also




<a href="https://msdn.microsoft.com/10e95100-4890-4c00-b231-bb7125fed197">IWSDSignatureProperty</a>
 

 


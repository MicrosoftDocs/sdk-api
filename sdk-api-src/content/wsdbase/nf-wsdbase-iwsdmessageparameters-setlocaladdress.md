---
UID: NF:wsdbase.IWSDMessageParameters.SetLocalAddress
title: IWSDMessageParameters::SetLocalAddress
author: windows-sdk-content
description: Sets a generic address object representing the source address that should send the message.
old-location: ncd\iwsdmessageparameters_setlocaladdress.htm
old-project: wsdapi
ms.assetid: 8266f091-9c88-44eb-a32b-1ff3da5fa10e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSDMessageParameters interface,SetLocalAddress method, IWSDMessageParameters.SetLocalAddress, IWSDMessageParameters::SetLocalAddress, SetLocalAddress, SetLocalAddress method, SetLocalAddress method,IWSDMessageParameters interface, ncd.iwsdmessageparameters_setlocaladdress, wsdbase/IWSDMessageParameters::SetLocalAddress
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDMessageParameters.SetLocalAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMessageParameters::SetLocalAddress


## -description


Sets a generic address object representing the source address that should send the message.


## -parameters




### -param pAddress [in]

An <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface that represents the source address that should send the message.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 


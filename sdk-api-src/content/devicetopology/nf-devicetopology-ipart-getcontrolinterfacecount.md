---
UID: NF:devicetopology.IPart.GetControlInterfaceCount
title: IPart::GetControlInterfaceCount
author: windows-sdk-content
description: The GetControlInterfaceCount method gets the number of control interfaces that this part supports.
old-location: coreaudio\ipart_getcontrolinterfacecount.htm
old-project: CoreAudio
ms.assetid: 8b82f69a-9b15-4bdf-9676-f2015ed67cfc
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetControlInterfaceCount, GetControlInterfaceCount method [Core Audio], GetControlInterfaceCount method [Core Audio],IPart interface, IPart interface [Core Audio],GetControlInterfaceCount method, IPart.GetControlInterfaceCount, IPart::GetControlInterfaceCount, IPartGetControlInterfaceCount, coreaudio.ipart_getcontrolinterfacecount, devicetopology/IPart::GetControlInterfaceCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: devicetopology.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPart.GetControlInterfaceCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPart::GetControlInterfaceCount


## -description



The <b>GetControlInterfaceCount</b> method gets the number of control interfaces that this part supports.




## -parameters




### -param pCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of control interfaces on this part.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


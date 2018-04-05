---
UID: NF:devicetopology.IPart.GetName
title: IPart::GetName method
author: windows-driver-content
description: The GetName method gets the friendly name of this part.
old-location: coreaudio\ipart_getname.htm
old-project: CoreAudio
ms.assetid: a583f445-ebb2-4072-a272-6f186aef71b3
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetName method [Core Audio], GetName method [Core Audio], IPart interface, GetName,IPart.GetName, IPart, IPart interface [Core Audio], GetName method, IPart::GetName, IPartGetName, coreaudio.ipart_getname, devicetopology/IPart::GetName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: devicetopology.h
req.include-header: 
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
req.typenames: ConnectorType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IPart.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPart::GetName method


## -description



The <b>GetName</b> method gets the friendly name of this part.




## -parameters




### -param ppwstrName [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the friendly name of this part. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetName</b> call fails,  <i>*ppwstrName</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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
Pointer <i>ppwstrName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


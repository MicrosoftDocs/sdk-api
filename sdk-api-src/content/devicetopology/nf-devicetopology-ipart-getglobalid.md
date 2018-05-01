---
UID: NF:devicetopology.IPart.GetGlobalId
title: IPart::GetGlobalId method
author: windows-driver-content
description: The GetGlobalId method gets the global ID of this part.
old-location: coreaudio\ipart_getglobalid.htm
old-project: CoreAudio
ms.assetid: 07825373-3ab2-42d3-8c4b-4eaf2c45eb95
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: GetGlobalId method [Core Audio], GetGlobalId method [Core Audio], IPart interface, GetGlobalId,IPart.GetGlobalId, IPart, IPart interface [Core Audio], GetGlobalId method, IPart::GetGlobalId, IPartGetGlobalId, coreaudio.ipart_getglobalid, devicetopology/IPart::GetGlobalId
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
-	IPart.GetGlobalId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPart::GetGlobalId method


## -description



The <b>GetGlobalId</b> method gets the global ID of this part.




## -parameters




### -param ppwstrGlobalId [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the global ID. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetGlobalId</b> call fails,  <i>*ppwstrGlobalId</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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
Pointer <i>ppwstrGlobalId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



A global ID is a string that uniquely identifies a part among all parts in all device topologies in the system. Clients should treat this string as opaque. That is, clients should <i>not</i> attempt to parse the contents of the string to obtain information about the part. The reason is that the string format is undefined and might change from one implementation of the DeviceTopology API to the next.




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


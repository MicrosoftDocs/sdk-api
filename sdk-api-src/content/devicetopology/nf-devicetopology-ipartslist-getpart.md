---
UID: NF:devicetopology.IPartsList.GetPart
title: IPartsList::GetPart
author: windows-sdk-content
description: The GetPart method gets a part from the parts list.
old-location: coreaudio\ipartslist_getpart.htm
tech.root: CoreAudio
ms.assetid: 505e2412-2849-4e64-9751-ce68831823b8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetPart, GetPart method [Core Audio], GetPart method [Core Audio],IPartsList interface, IPartsList interface [Core Audio],GetPart method, IPartsList.GetPart, IPartsList::GetPart, IPartsListGetPart, coreaudio.ipartslist_getpart, devicetopology/IPartsList::GetPart
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPartsList.GetPart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPartsList::GetPart


## -description



The <b>GetPart</b> method gets a part from the parts list.




## -parameters




### -param nIndex [in]

The part number of the part to retrieve. If the parts list contains <i>n</i> parts, the parts are numbered 0 to <i>n</i>– 1. Call the <a href="https://msdn.microsoft.com/78ca8592-f687-4194-873b-83640c6e72da">IPartsList::GetCount</a> method to get the number of parts in the list.


### -param ppPart [out]

Pointer to a pointer variable into which the method writes the address of the <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface of the part object. Through this method, the caller obtains a counted reference to the <b>IPart</b> interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetPart</b> call fails,  <i>*ppPart</i> is <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nIndex</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppPart</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For a code example that calls the <b>GetPart</b> method, see the implementation of the SelectCaptureDevice function in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -see-also




<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/3ac48781-90c2-4b23-aa68-3453091bde61">IPartsList Interface</a>



<a href="https://msdn.microsoft.com/78ca8592-f687-4194-873b-83640c6e72da">IPartsList::GetCount</a>
 

 


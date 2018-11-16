---
UID: NF:devicetopology.IPart.GetLocalId
title: IPart::GetLocalId
author: windows-sdk-content
description: The GetLocalId method gets the local ID of this part.
old-location: coreaudio\ipart_getlocalid.htm
tech.root: CoreAudio
ms.assetid: d5ca4908-1822-485c-a04a-0eeee1e384a8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLocalId, GetLocalId method [Core Audio], GetLocalId method [Core Audio],IPart interface, IPart interface [Core Audio],GetLocalId method, IPart.GetLocalId, IPart::GetLocalId, IPartGetLocalId, coreaudio.ipart_getlocalid, devicetopology/IPart::GetLocalId
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
 - IPart.GetLocalId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- devicetopology.h
: 
- IPart.GetLocalId
: 
---

# IPart::GetLocalId


## -description



The <b>GetLocalId</b> method gets the local ID of this part.




## -parameters




### -param pnId [out]

Pointer to a <b>UINT</b> variable into which the method writes the local ID of this part.


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
Pointer <i>pnId</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When you have a pointer to a part object, you can call this method to get the local ID of the part. A local ID is a number that uniquely identifies a part among all parts in a device topology.

The <a href="https://msdn.microsoft.com/38288a63-62a3-4b06-b2e6-dbe8c27e09ad">IAudioInputSelector::GetSelection</a> and <a href="https://msdn.microsoft.com/af4b1a1d-b08d-4165-a011-bdbd1e063e74">IAudioOutputSelector::GetSelection</a> methods retrieve the local ID of a connected part. The <a href="https://msdn.microsoft.com/b6291447-d3a9-4bc7-808c-9427e1642752">IAudioInputSelector::SetSelection</a> and <a href="https://msdn.microsoft.com/e81d54f4-1451-4bd0-be06-28ff01fb65ab">IAudioOutputSelector::SetSelection</a> methods select the input or output that is connected to a part that is identified by its local ID. The <a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a> method gets a part that is identified by its local ID.

For code examples that use the <b>GetLocalId</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72bf9164-96c6-4543-b858-19480b032fdb">Using the IKsControl Interface to Access Audio Properties</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/38288a63-62a3-4b06-b2e6-dbe8c27e09ad">IAudioInputSelector::GetSelection</a>



<a href="https://msdn.microsoft.com/b6291447-d3a9-4bc7-808c-9427e1642752">IAudioInputSelector::SetSelection</a>



<a href="https://msdn.microsoft.com/af4b1a1d-b08d-4165-a011-bdbd1e063e74">IAudioOutputSelector::GetSelection</a>



<a href="https://msdn.microsoft.com/e81d54f4-1451-4bd0-be06-28ff01fb65ab">IAudioOutputSelector::SetSelection</a>



<a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


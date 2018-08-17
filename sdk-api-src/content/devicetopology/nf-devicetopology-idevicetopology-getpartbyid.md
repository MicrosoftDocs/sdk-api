---
UID: NF:devicetopology.IDeviceTopology.GetPartById
title: IDeviceTopology::GetPartById
author: windows-sdk-content
description: The GetPartById method gets a part that is identified by its local ID.
old-location: coreaudio\idevicetopology_getpartbyid.htm
old-project: CoreAudio
ms.assetid: 03310040-2081-47cf-88aa-6281c6bea56e
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetPartById, GetPartById method [Core Audio], GetPartById method [Core Audio],IDeviceTopology interface, IDeviceTopology interface [Core Audio],GetPartById method, IDeviceTopology.GetPartById, IDeviceTopology::GetPartById, IDeviceTopologyGetPartById, coreaudio.idevicetopology_getpartbyid, devicetopology/IDeviceTopology::GetPartById
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
 - IDeviceTopology.GetPartById
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDeviceTopology::GetPartById


## -description



The <b>GetPartById</b> method gets a part that is identified by its local ID.




## -parameters




### -param nId [in]

The part to get. This parameter is the local ID of the part. For more information, see Remarks.


### -param ppPart [out]

Pointer to a pointer variable into which the method writes the address of the <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface of the part object that is identified by <i>nId</i>. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetPartById</b> call fails,  <i>*ppPart</i> is <b>NULL</b>.


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
Parameter <i>nId</i> is not a valid local ID.

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



A local ID is a number that uniquely identifies a part among all the parts in a device topology. The <a href="https://msdn.microsoft.com/38288a63-62a3-4b06-b2e6-dbe8c27e09ad">IAudioInputSelector::GetSelection</a> and <a href="https://msdn.microsoft.com/af4b1a1d-b08d-4165-a011-bdbd1e063e74">IAudioOutputSelector::GetSelection</a> methods retrieve the local ID of a connected part. The <a href="https://msdn.microsoft.com/b6291447-d3a9-4bc7-808c-9427e1642752">IAudioInputSelector::SetSelection</a> and <a href="https://msdn.microsoft.com/e81d54f4-1451-4bd0-be06-28ff01fb65ab">IAudioOutputSelector::SetSelection</a> methods select the input or output that is connected to a part that is identified by its local ID. When you have a pointer to a part object, you can call the <a href="https://msdn.microsoft.com/d5ca4908-1822-485c-a04a-0eeee1e384a8">IPart::GetLocalId</a> method to get the local ID of the part.




## -see-also




<a href="https://msdn.microsoft.com/38288a63-62a3-4b06-b2e6-dbe8c27e09ad">IAudioInputSelector::GetSelection</a>



<a href="https://msdn.microsoft.com/b6291447-d3a9-4bc7-808c-9427e1642752">IAudioInputSelector::SetSelection</a>



<a href="https://msdn.microsoft.com/af4b1a1d-b08d-4165-a011-bdbd1e063e74">IAudioOutputSelector::GetSelection</a>



<a href="https://msdn.microsoft.com/e81d54f4-1451-4bd0-be06-28ff01fb65ab">IAudioOutputSelector::SetSelection</a>



<a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology Interface</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/d5ca4908-1822-485c-a04a-0eeee1e384a8">IPart::GetLocalId</a>
 

 


---
UID: NF:devicetopology.IAudioInputSelector.GetSelection
title: IAudioInputSelector::GetSelection
author: windows-sdk-content
description: The GetSelection method gets the local ID of the part that is connected to the selector input that is currently selected.
old-location: coreaudio\iaudioinputselector_getselection.htm
tech.root: CoreAudio
ms.assetid: 38288a63-62a3-4b06-b2e6-dbe8c27e09ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSelection, GetSelection method [Core Audio], GetSelection method [Core Audio],IAudioInputSelector interface, IAudioInputSelector interface [Core Audio],GetSelection method, IAudioInputSelector.GetSelection, IAudioInputSelector::GetSelection, IAudioInputSelectorGetSelection, coreaudio.iaudioinputselector_getselection, devicetopology/IAudioInputSelector::GetSelection
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
 - IAudioInputSelector.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioInputSelector::GetSelection


## -description



The GetSelection method gets the local ID of the part that is connected to the selector input that is currently selected.




## -parameters




### -param pnIdSelected [out]

Pointer to a <b>UINT</b> variable into which the method writes the local ID of the part that directly links to the currently selected selector input.


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
Pointer <i>pnIdSelected</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



A local ID is a number that uniquely identifies a part among all parts in a device topology. To obtain a pointer to the <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface of a part from its local ID, call the <a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6f5ce9c0-39e4-4fab-910c-9a11b90fcde7">IAudioInputSelector Interface</a>



<a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


---
UID: NF:devicetopology.IAudioOutputSelector.GetSelection
title: IAudioOutputSelector::GetSelection method
author: windows-driver-content
description: The GetSelection method gets the local ID of the part that is connected to the selector output that is currently selected.
old-location: coreaudio\iaudiooutputselector_getselection.htm
old-project: CoreAudio
ms.assetid: af4b1a1d-b08d-4165-a011-bdbd1e063e74
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: GetSelection method [Core Audio], GetSelection method [Core Audio], IAudioOutputSelector interface, GetSelection,IAudioOutputSelector.GetSelection, IAudioOutputSelector, IAudioOutputSelector interface [Core Audio], GetSelection method, IAudioOutputSelector::GetSelection, IAudioOutputSelectorGetSelection, coreaudio.iaudiooutputselector_getselection, devicetopology/IAudioOutputSelector::GetSelection
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
-	IAudioOutputSelector.GetSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioOutputSelector::GetSelection method


## -description



The <b>GetSelection</b> method gets the local ID of the part that is connected to the selector output that is currently selected.




## -parameters




### -param pnIdSelected [out]

Pointer to a <b>UINT</b> variable into which the method writes the local ID of the part that has a direct link to the currently selected selector output.


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




<a href="https://msdn.microsoft.com/571a44b6-972f-4d75-a31f-0e02cf728764">IAudioOutputSelector Interface</a>



<a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 


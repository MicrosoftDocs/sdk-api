---
UID: NF:mmdeviceapi.IMMDeviceCollection.GetCount
title: IMMDeviceCollection::GetCount
author: windows-sdk-content
description: The GetCount method retrieves a count of the devices in the device collection.
old-location: coreaudio\immdevicecollection_getcount.htm
old-project: CoreAudio
ms.assetid: 236a611b-98ab-437c-9e36-8c8a7c32ffbc
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetCount, GetCount method [Core Audio], GetCount method [Core Audio],IMMDeviceCollection interface, IMMDeviceCollection interface [Core Audio],GetCount method, IMMDeviceCollection.GetCount, IMMDeviceCollection::GetCount, IMMDeviceCollectionGetCount, coreaudio.immdevicecollection_getcount, mmdeviceapi/IMMDeviceCollection::GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmdeviceapi.h
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
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDeviceCollection.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMMDeviceCollection::GetCount


## -description



The <b>GetCount</b> method retrieves a count of the devices in the device collection.




## -parameters




### -param pcDevices [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of devices in the device collection.


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
Parameter <i>pcDevices</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For a code example that calls the <b>GetCount</b> method, see <a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>.




## -see-also




<a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection Interface</a>
 

 


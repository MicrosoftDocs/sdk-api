---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWiaItem::EnumDeviceCapabilities


## -description


The <b>IWiaItem::EnumDeviceCapabilities</b> method creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) device supports.


## -parameters




### -param lFlags [in]

Type: <b>LONG</b>

Specifies a flag that selects the type of capabilities to enumerate. Can be set to one or more of the following values:



<table class="clsStd">
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_DEVICE_COMMANDS</td>
<td>Enumerate device commands.</td>
</tr>
<tr>
<td>WIA_DEVICE_EVENTS</td>
<td>Enumerate device events.</td>
</tr>
</table>
 


### -param ppIEnumWIA_DEV_CAPS [out]

Type: <b><a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a>**</b>

Pointer to <a href="https://msdn.microsoft.com/736a8aba-58e0-4b52-a997-ef1fb80473ba">IEnumWIA_DEV_CAPS</a> interface created by <b>IWiaItem::EnumDeviceCapabilities</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use this method to create an enumerator object to obtain the set of commands and events that a WIA device supports. You can use the <i>lFlags</i> parameter to specify which kinds of device capabilities to enumerate. The <b>IWiaItem::EnumDeviceCapabilities</b> method stores the address of the interface of the enumerator object in the <i>ppIEnumWIA_DEV_CAPS</i> parameter.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnumWIA_DEV_CAPS</i> parameter.




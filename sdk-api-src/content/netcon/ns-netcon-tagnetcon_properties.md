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

# tagNETCON_PROPERTIES structure


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>NETCON_PROPERTIES</b> structure stores values that describe the properties of a network connection.


## -struct-fields




### -field guidId

Globally-unique identifier (GUID) for this connection.


### -field pszwName

Name of the connection itself.


### -field pszwDeviceName

Name of the device associated with the connection.


### -field Status


<a href="https://msdn.microsoft.com/feb0aa60-b873-4536-8ec2-2dce4d355fdb">Current status</a> of the connection.


### -field MediaType


<a href="https://msdn.microsoft.com/9236371c-0e3f-43ba-a02f-0770768008ae">Media type</a> associated with this connection.


### -field dwCharacter


<a href="https://msdn.microsoft.com/library/windows/hardware/dn949900">Characteristics</a> for this connection.


### -field clsidThisObject

Class identifier for the connection object.


### -field clsidUiObject

Class identifier for the user-interface object.


## -see-also




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall
		  Reference</a>



<a href="https://msdn.microsoft.com/483d7cd5-5db6-4af3-964b-3f7cd2e4f8a8">Internet Connection Sharing and Internet Connection Firewall
		  Structures</a>



<a href="https://msdn.microsoft.com/fc64c840-7f88-4d81-910b-3cf21dce70fa">NETCON_CHARACTERISTIC_FLAGS</a>



<a href="https://msdn.microsoft.com/9236371c-0e3f-43ba-a02f-0770768008ae">NETCON_MEDIATYPE</a>



<a href="https://msdn.microsoft.com/feb0aa60-b873-4536-8ec2-2dce4d355fdb">NETCON_STATUS</a>
 

 


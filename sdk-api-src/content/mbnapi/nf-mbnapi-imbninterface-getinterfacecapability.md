---
UID: NF:mbnapi.IMbnInterface.GetInterfaceCapability
title: IMbnInterface::GetInterfaceCapability
author: windows-sdk-content
description: Gets the capabilities of the device.
old-location: mbn\imbninterface_getinterfacecapability.htm
old-project: mbn
ms.assetid: cfe8f638-ad17-4118-9c79-b7ebc81c726a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetInterfaceCapability, GetInterfaceCapability method [Microsoft Broadband Networks], GetInterfaceCapability method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetInterfaceCapability method, IMbnInterface.GetInterfaceCapability, IMbnInterface::GetInterfaceCapability, mbn.imbninterface_getinterfacecapability, mbnapi/IMbnInterface::GetInterfaceCapability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterface.GetInterfaceCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterface::GetInterfaceCapability


## -description


Gets the capabilities of the device.


## -parameters




### -param interfaceCaps [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a> structure that contains the interface capabilities.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.  <i>interfaceCaps</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for the device capabilities.  The calling application can get notified when the device capabilities are available by registering for the <a href="https://msdn.microsoft.com/eeeffe13-307b-45f3-aa24-c33c621aa18e">OnInterfaceCapabilityAvailable</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>GetInterfaceCapability</b> method returns the interface capabilities, including the cellular technology type, the type of support for voice calls, the type of SIM used, the frequency bands supported, and the availability of SMS support. It also returns the device manufacturer name, model, and firmware name, though these are optional and may not be filled for some of the devices. For more information, see <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a>.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 


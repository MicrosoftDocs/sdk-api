---
UID: NF:mbnapi.IMbnInterface.InEmergencyMode
title: IMbnInterface::InEmergencyMode
author: windows-sdk-content
description: Determines whether the device is in emergency mode.
old-location: mbn\imbninterface_inemergencymode.htm
old-project: mbn
ms.assetid: b4ce2c10-627d-4cbe-a884-7bb8731c3bcf
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnInterface interface [Microsoft Broadband Networks],InEmergencyMode method, IMbnInterface.InEmergencyMode, IMbnInterface::InEmergencyMode, InEmergencyMode, InEmergencyMode method [Microsoft Broadband Networks], InEmergencyMode method [Microsoft Broadband Networks],IMbnInterface interface, mbn.imbninterface_inemergencymode, mbnapi/IMbnInterface::InEmergencyMode
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
 - IMbnInterface.InEmergencyMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterface::InEmergencyMode


## -description


Determines whether the device is in emergency mode.


## -parameters




### -param emergencyMode [out]

Points to VARIANT_TRUE if the device is in emergency mode, and VARIANT_FALSE if it is not.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for this information.  The calling application can be notified when the data is available by registering for the <a href="https://msdn.microsoft.com/637e0f6b-102f-436c-b0ec-edef16245675">OnEmergencyModeChange</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>
 




## -remarks



If a device cannot register on the network for any reason, then the device may automatically register onto a network in emergency mode. For example, a device cannot register on the network if the SIM is not inserted, user subscription validity expired, or roaming is not enabled for user.  In emergency mode, device can be used in limited mode for voice calls to emergency numbers.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 


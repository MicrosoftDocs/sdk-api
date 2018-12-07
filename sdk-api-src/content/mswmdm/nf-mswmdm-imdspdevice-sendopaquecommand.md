---
UID: NF:mswmdm.IMDSPDevice.SendOpaqueCommand
title: IMDSPDevice::SendOpaqueCommand
author: windows-sdk-content
description: The SendOpaqueCommand method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.
old-location: wmdm\imdspdevice_sendopaquecommand.htm
tech.root: WMDM
ms.assetid: d7b60187-84d1-4ff3-ab58-e6b8ea75ee37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMDSPDevice interface [windows Media Device Manager],SendOpaqueCommand method, IMDSPDevice.SendOpaqueCommand, IMDSPDevice::SendOpaqueCommand, IMDSPDeviceSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IMDSPDevice interface, mswmdm/IMDSPDevice::SendOpaqueCommand, wmdm.imdspdevice_sendopaquecommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice.SendOpaqueCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPDevice::SendOpaqueCommand


## -description



The <b>SendOpaqueCommand</b> method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.




## -parameters




### -param pCommand [in, out]

Pointer to an <a href="https://msdn.microsoft.com/5b39cf07-2816-4615-a754-e3f0c57bf4ce">OPAQUECOMMAND</a> structure containing the information required to execute the command.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is used with device commands that do not affect Windows Media Device Manager, and are passed through unchanged. A more efficient way to call commands on a device is to call <a href="https://msdn.microsoft.com/1f41c3f9-8eb6-4d51-87f9-c8b035a73cce">IMDSPDevice3::DeviceIoControl</a>.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>
 

 


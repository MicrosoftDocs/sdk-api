---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedCommands
title: IPortableDeviceCapabilities::GetSupportedCommands
author: windows-sdk-content
description: The GetSupportedCommands method retrieves a list of all the supported commands for this device.
old-location: wpdsdk\iportabledevicecapabilities_getsupportedcommands.htm
old-project: wpd_sdk
ms.assetid: 974b16c7-27a0-40a6-8941-e93293a69b48
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSupportedCommands, GetSupportedCommands method [Windows Portable Devices SDK], GetSupportedCommands method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedCommands method, IPortableDeviceCapabilities.GetSupportedCommands, IPortableDeviceCapabilities::GetSupportedCommands, IPortableDeviceCapabilitiesGetSupportedCommands, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedCommands, wpdsdk.iportabledevicecapabilities_getsupportedcommands
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceCapabilities.GetSupportedCommands
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceCapabilities::GetSupportedCommands


## -description


The <b>GetSupportedCommands</b> method retrieves a list of all the supported commands for this device.
      


## -parameters




### -param ppCommands [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd">IPortableDeviceKeyCollection</a> interface that holds all the valid commands. For a list of commands that are defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/f579745a-5327-4c8b-bfa7-fe81d9657a3b">Commands</a>. The caller must release this interface when it is done with it.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



None.
      




## -see-also




<a href="wpdsdk.iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>
 

 


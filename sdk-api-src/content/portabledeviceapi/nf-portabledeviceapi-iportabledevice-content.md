---
UID: NF:portabledeviceapi.IPortableDevice.Content
title: IPortableDevice::Content
author: windows-sdk-content
description: The Content method retrieves an interface that you can use to access objects on a device.
old-location: wpdsdk\iportabledevice_content.htm
old-project: wpd_sdk
ms.assetid: f65ff0b5-ca3b-498f-9c5e-36a76104d220
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Content, Content method [Windows Portable Devices SDK], Content method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Content method, IPortableDevice.Content, IPortableDevice::Content, IPortableDeviceContent, portabledeviceapi/IPortableDevice::Content, wpdsdk.iportabledevice_content
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
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
 - IPortableDevice.Content
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDevice::Content


## -description



        The <b>Content</b> method retrieves an interface that you can use to access objects on a device.
      


## -parameters




### -param ppContent [out]


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/Dd388529(v=VS.85).aspx">IPortableDeviceContent</a> interface that is used to access the content on a device. The caller must release this interface when it is done with it.
          


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppContent</i> argument was a NULL pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/81476f50-5ea0-4e02-9e38-2b1dfcc32c4f">Adding a Resource to an Object</a>



<a href="https://msdn.microsoft.com/86782a09-4fca-4ae0-beaf-296069e061dc">Enumerating Content</a>



<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>



<a href="https://msdn.microsoft.com/5072d308-d376-4141-96df-dbef23fb9f9b">Moving Content on the Device</a>



<a href="https://msdn.microsoft.com/0d0c6b3d-23bc-4628-a684-14bb9e18967f">Retrieving Properties for Multiple Objects</a>



<a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>



<a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a>



<a href="https://msdn.microsoft.com/0686ba54-4782-42a4-8fdb-2325fc8d8bc2">Setting Properties for Multiple Objects</a>



<a href="https://msdn.microsoft.com/1c003534-96b4-419b-94d1-73b5ffa2eba1">Setting Properties for a Single Object</a>
 

 


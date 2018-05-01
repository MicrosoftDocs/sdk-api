---
UID: NF:portabledeviceapi.IPortableDevice.Advise
title: IPortableDevice::Advise method
author: windows-driver-content
description: The Advise method registers an application-defined callback that receives device events.
old-location: wpdsdk\iportabledevice_advise.htm
old-project: wpd_sdk
ms.assetid: bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: Advise method [Windows Portable Devices SDK], Advise method [Windows Portable Devices SDK], IPortableDevice interface, Advise,IPortableDevice.Advise, IPortableDevice, IPortableDevice interface [Windows Portable Devices SDK], Advise method, IPortableDevice::Advise, IPortableDeviceAdvise, portabledeviceapi/IPortableDevice::Advise, wpdsdk.iportabledevice_advise
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevice.Advise
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDevice::Advise method


## -description



        The <b>Advise</b> method registers an application-defined callback that receives device events.
      


## -parameters




### -param dwFlags [in]

<b>DWORD</b> that specifies option flags.
          


### -param pCallback [in]


            Pointer to a callback object.
          


### -param pParameters [in]


            This parameter is ignored and should be set to <b>NULL</b>.
          


### -param ppszCookie [out]


            A string that represents a unique context ID. This is used to unregister for callbacks when calling <a href="https://msdn.microsoft.com/6720e92b-35cd-4e3f-bd21-36337cf80140">Unadvise</a>.
          


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
The application-defined callback was successfully registered.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>



<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>
 

 


---
UID: NF:mswmdm.IWMDMDevice3.SetProperty
title: IWMDMDevice3::SetProperty
author: windows-sdk-content
description: The SetProperty method sets a specific device property, if it is writable.
old-location: wmdm\iwmdmdevice3_setproperty.htm
tech.root: WMDM
ms.assetid: 39483d9a-0725-45fa-9d41-dbabd400b3bf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMDevice3 interface [windows Media Device Manager],SetProperty method, IWMDMDevice3.SetProperty, IWMDMDevice3::SetProperty, IWMDMDevice3SetProperty, SetProperty, SetProperty method [windows Media Device Manager], SetProperty method [windows Media Device Manager],IWMDMDevice3 interface, mswmdm/IWMDMDevice3::SetProperty, wmdm.iwmdmdevice3_setproperty
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
 - IWMDMDevice3.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IWMDMDevice3.SetProperty
: 
---

# IWMDMDevice3::SetProperty


## -description



The <b>SetProperty</b> method sets a specific device property, if it is writable.




## -parameters




### -param pwszPropName [in]

A wide character, null-terminated string name of the property to set. This overwrites any existing property with the same name. Once the application has made this call, it should free any dynamic memory using <b>PropVariantClear</b>. A list of standard property name constants is given in <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.


### -param pValue [in]

Value of the property being set.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method sets the specified device property. To obtain the list of supported device properties, the client should query the <a href="https://msdn.microsoft.com/f1c8406f-f0cb-4def-bc26-399908ecbf83">IWMDMDevice3::GetProperty</a> method for the <b>g_wszWMDMSupportedDeviceProperties</b> property.

For the list of device property names, see <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.

This method is similar to the <b>SetMetadata</b> method for storages, but this method can set only one property at one time.

Not all properties of the device can be set.




## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>



<a href="https://msdn.microsoft.com/f1c8406f-f0cb-4def-bc26-399908ecbf83">IWMDMDevice3::GetProperty</a>



<a href="https://msdn.microsoft.com/f06eb965-af34-4247-b8a6-0ac1ee4e4839">IWMDMStorage3::SetMetadata</a>



<a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 


---
UID: NF:mswmdm.IWMDMEnumDevice.Next
title: IWMDMEnumDevice::Next
author: windows-sdk-content
description: The Next method returns a pointer to the next device, represented by an IWMDMDevice interface.
old-location: wmdm\iwmdmenumdevice_next.htm
old-project: WMDM
ms.assetid: 75a5961f-2c61-4e10-a570-7ebfabb97367
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWMDMEnumDevice interface [windows Media Device Manager],Next method, IWMDMEnumDevice.Next, IWMDMEnumDevice::Next, IWMDMEnumDeviceNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IWMDMEnumDevice interface, mswmdm/IWMDMEnumDevice::Next, wmdm.iwmdmenumdevice_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMEnumDevice.Next
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMEnumDevice::Next


## -description



The <b>Next</b> method returns a pointer to the next device, represented by an <a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice</a> interface.




## -parameters




### -param celt [in]

Number of devices requested.


### -param ppDevice [out]

Pointer to caller-allocated array of <a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice</a> interface pointers. The size of this array must be <b>IWMDMDevice</b> *[celt]. The caller must release these interfaces when done with them. To avoid allocating a whole array, simply pass in the address of a pointer to an <b>IWMDMDevice</b> interface, as shown in Remarks.


### -param pceltFetched [out]

Pointer to a variable that receives the number of devices (interfaces) returned.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The returned device interface(s) are based on a cached list of devices. If a Plug and Play device is attached or removed, the current enumerator will not reflect that, and therefore, <b>Next</b> will return devices based on the cached list. Applications should obtain a new enumerator object by calling <a href="https://msdn.microsoft.com/1daa6d36-9858-4504-a9a2-c0341031829b">IWMDeviceManager::EnumDevices</a> to get a refreshed list of devices.

If you only want to retrieve a single interface at a time, you do not need to allocate an array for this method, as shown in the following code:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get a device enumerator to examine each device.
CComPtr&lt;IWMDeviceManager2&gt; pIWMDevMgr2;
hr = m_IWMDeviceMgr-&gt;QueryInterface (__uuidof(IWMDeviceManager2), (void**) &amp;pIWMDevMgr2);
if (hr == S_OK)
{
    // TODO: Display a message that the application retrieved IWMDeviceManager2.
}
else
{
    // TODO: Display a message that the application was not able to 
    // retrieve IWMDeviceManager2 in EnumDevices.
    return hr;
}

// Enumerate through the devices using the faster EnumDevices2 plug-and-play method.
CComPtr&lt;IWMDMEnumDevice&gt; pEnumDevice;
hr = pIWMDevMgr2-&gt;EnumDevices2(&amp;pEnumDevice);
if (hr != S_OK)
{
    //.TODO: Display a message that an error occurred in calling EnumDevices2.
    return hr;
}

// Enumerate through devices.
IWMDMDevice *pIWMDMDevice;
ULONG ulFetched = 0;
while(pEnumDevice-&gt;Next(1, &amp;pIWMDMDevice, &amp;ulFetched) == S_OK)
{
    if (ulFetched != 1)
    {
        return E_FAIL;
    }
    // Do some stuff here....
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice Interface</a>



<a href="https://msdn.microsoft.com/1daa6d36-9858-4504-a9a2-c0341031829b">IWMDeviceManager::EnumDevices</a>
 

 


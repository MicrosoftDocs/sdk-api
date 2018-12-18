---
UID: NF:portabledeviceapi.IPortableDevice.Open
title: IPortableDevice::Open
author: windows-sdk-content
description: The Open method opens a connection between the application and the device.
old-location: wpdsdk\iportabledevice_open.htm
tech.root: wpd_sdk
ms.assetid: d505fc34-9b6d-417a-a53e-e74773dcc8a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPortableDevice interface [Windows Portable Devices SDK],Open method, IPortableDevice.Open, IPortableDevice::Open, IPortableDeviceOpen, Open, Open method [Windows Portable Devices SDK], Open method [Windows Portable Devices SDK],IPortableDevice interface, portabledeviceapi/IPortableDevice::Open, wpdsdk.iportabledevice_open
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDevice::Open


## -description


The <b>Open</b> method opens a connection between the application and the device.
      


## -parameters




### -param pszPnPDeviceID [in]

A pointer to a null-terminated string that contains the Plug and Play ID string for the device. You can get this string by calling <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a>.
          


### -param pClientInfo [in]

A pointer to an <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that holds information that identifies the application to the device. This interface holds <b>PROPERTYKEY</b>/value pairs that try to identify an application uniquely. Although the presence of a CoCreated interface is required, the application is not required to send any key/value pairs. However, sending data might improve performance. Typical key/value pairs include the application name, major and minor version, and build number.

 See properties beginning with "WPD_CLIENT_" in the <a href="https://msdn.microsoft.com/3bfbe8d0-6ad5-42de-afdd-d83328aaaa62">Properties</a> section.
          


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
<dt><b>E_WPD_DEVICE_ALREADY_OPENED</b></dt>
</dl>
</td>
<td width="60%">
The device connection has already been opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the arguments was a NULL pointer.

</td>
</tr>
</table>
 




## -remarks



A device must be opened before you can call any methods on it. (Note that the <a href="https://msdn.microsoft.com/11cd5b2b-e8f8-4ba1-8527-f7a403f399d5">IPortableDeviceManager</a> methods do not require you to open a device before calling any methods.) However, usually you do not need to call <a href="https://msdn.microsoft.com/aa60a439-7589-465e-98e5-56b93d594f96">Close</a>.

Administrators can restrict the access of portable devices to computers running on a network. For example, an administrator may restrict all Guest users to read-only access, while Authenticated users are given read/write access.
      

Due to these security issues, if your application will not perform write operations, it should call the <b>Open</b> method and request read-only access by specifying GENERIC_READ for the WPD_CLIENT_DESIRED_ACCESS property that it supplies in the <i>pClientInfo</i> parameter.
      

If your application requires write operations, it should call the <b>Open</b> method as shown in the following example code. The first time, it should request read/write access by passing the default WPD_CLIENT_DESIRED_ACCESS property in the <i>pClientInfo</i> parameter. If this first call fails and returns E_ACCESSDENIED, your application should call the <b>Open</b> method a second time and request read-only access by specifying GENERIC_READ for the WPD_CLIENT_DESIRED_ACCESS property that it supplies in the <i>pClientInfo</i> parameter.

Applications that live in Single Threaded Apartments should use <b>CLSID_PortableDeviceFTM</b>, as this eliminates the overhead of interface pointer marshaling.  <b>CLSID_PortableDevice</b> is still supported for legacy applications.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define CLIENT_NAME         L"My WPD Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     0

HRESULT OpenDevice(LPCWSTR wszPnPDeviceID, IPortableDevice** ppDevice)
{
    HRESULT                hr                 = S_OK;
    IPortableDeviceValues* pClientInformation = NULL;
    IPortableDevice*       pDevice            = NULL;

    if ((wszPnPDeviceID == NULL) || (ppDevice == NULL))
    {
        hr = E_INVALIDARG;
        return hr;
    }

    // CoCreate an IPortableDeviceValues interface to hold the client information.
    hr = CoCreateInstance(CLSID_PortableDeviceValues,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValues,
                          (VOID**) &amp;pClientInformation);
    if (SUCCEEDED(hr))
    {
        HRESULT ClientInfoHR = S_OK;

        // Attempt to set all properties for client information. If we fail to set
        // any of the properties below it is OK. Failing to set a property in the
        // client information isn't a fatal error.
        ClientInfoHR = pClientInformation-&gt;SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
        if (FAILED(ClientInfoHR))
        {
           // Failed to set WPD_CLIENT_NAME
        }

        ClientInfoHR = pClientInformation-&gt;SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
        if (FAILED(ClientInfoHR))
        {
            // Failed to set WPD_CLIENT_MAJOR_VERSION
        }

        ClientInfoHR = pClientInformation-&gt;SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
        if (FAILED(ClientInfoHR))
        {
            // Failed to set WPD_CLIENT_MINOR_VERSION
        }

        ClientInfoHR = pClientInformation-&gt;SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
        if (FAILED(ClientInfoHR))
        {
            // Failed to set WPD_CLIENT_REVISION
        }
    }
    else
    {
        // Failed to CoCreateInstance CLSID_PortableDeviceValues for client information
    }

        ClientInfoHR = pClientInformation-&gt;SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
        if (FAILED(ClientInfoHR))
        {
            // Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE
        }

    if (SUCCEEDED(hr))
    {
        // CoCreate an IPortableDevice interface
        hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDevice,
                              (VOID**) &amp;pDevice);

        if (SUCCEEDED(hr))
        {
            // Attempt to open the device using the PnPDeviceID string given
            // to this function and the newly created client information.
            // Note that we're attempting to open the device the first 
            // time using the default (read/write) access. If this fails
            // with E_ACCESSDENIED, we'll attempt to open a second time
            // with read-only access.
            hr = pDevice-&gt;Open(wszPnPDeviceID, pClientInformation);
            if (hr == E_ACCESSDENIED)
            {
                 // Attempt to open for read-only access
                 pClientInformation-&gt;SetUnsignedIntegerValue(
                       WPD_CLIENT_DESIRED_ACCESS,
                       GENERIC_READ);
                 hr = pDevice-&gt;Open(wszPnPDeviceID, pClientInformation);
            }
            if (SUCCEEDED(hr))
            {
                // The device successfully opened, obtain an instance of the Device into
                // ppDevice so the caller can be returned an opened IPortableDevice.
                hr = pDevice-&gt;QueryInterface(IID_IPortableDevice, (VOID**)ppDevice);
                if (FAILED(hr))
                {
                    // Failed to QueryInterface the opened IPortableDevice
                }
            }
        }
        else
        {
            // Failed to CoCreateInstance CLSID_PortableDevice
        }
    }

    // Release the IPortableDevice when finished
    if (pDevice != NULL)
    {
        pDevice-&gt;Release();
        pDevice = NULL;
    }

    // Release the IPortableDeviceValues that contains the client information when finished
    if (pClientInformation != NULL)
    {
        pClientInformation-&gt;Release();
        pClientInformation = NULL;
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/16286da5-5979-413b-a4db-ca157b10a571">Establishing a Connection</a>



<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>



<a href="https://msdn.microsoft.com/aa60a439-7589-465e-98e5-56b93d594f96">IPortableDevice::Close</a>
 

 


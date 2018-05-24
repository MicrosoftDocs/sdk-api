---
UID: NF:mswmdm.IWMDMDeviceControl.GetCapabilities
title: IWMDMDeviceControl::GetCapabilities
author: windows-driver-content
description: The GetCapabilities method retrieves the device capabilities to determine what operations the device can perform. The capabilities describe the methods of the device control that are supported by the media device.
old-location: wmdm\iwmdmdevicecontrol_getcapabilities.htm
old-project: WMDM
ms.assetid: 61d0e44c-f1be-4837-a773-48c6c5278fe0
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetCapabilities, GetCapabilities method [windows Media Device Manager], GetCapabilities method [windows Media Device Manager],IWMDMDeviceControl interface, IWMDMDeviceControl interface [windows Media Device Manager],GetCapabilities method, IWMDMDeviceControl.GetCapabilities, IWMDMDeviceControl::GetCapabilities, IWMDMDeviceControlGetCapabilities, mswmdm/IWMDMDeviceControl::GetCapabilities, wmdm.iwmdmdevicecontrol_getcapabilities
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMDeviceControl.GetCapabilities
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceControl::GetCapabilities


## -description



The <b>GetCapabilities</b> method retrieves the device capabilities to determine what operations the device can perform. The capabilities describe the methods of the device control that are supported by the media device.




## -parameters




### -param pdwCapabilitiesMask [out]

Pointer to a <b>DWORD</b> specifying the capabilities of the device. The following flags can be returned in this variable.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANPLAY</td>
<td>The media device can play MP3 audio.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTREAMPLAY</td>
<td>The media device can play streaming audio directly from the host computer.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANRECORD</td>
<td>The media device can record audio.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTREAMRECORD</td>
<td>The media device can record streaming audio directly to the host computer.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANPAUSE</td>
<td>The media device can pause during play or record operations.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANRESUME</td>
<td>The media device can resume an operation that was paused.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSTOP</td>
<td>The media device can stop playing before the end of a file.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_CANSEEK</td>
<td>The media device can seek to a position other than the beginning of a file.</td>
</tr>
<tr>
<td>WMDM_DEVICECAP_HASSECURECLOCK</td>
<td>The media device has a secure clock.</td>
</tr>
</table>
 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwCapabilitiesMask</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



Currently, not many devices report their capabilities correctly.


#### Examples

The following C++ code retrieves the device capabilities.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Examine the device capabilities.
// Use some of these to enable or disable the application's
// user interface elements.
CComQIPtr&lt;IWMDMDeviceControl&gt; pDeviceControl(pIWMDMDevice);
if (pDeviceControl != NULL)
{
    DWORD caps = 0;
    hr = pDeviceControl-&gt;GetCapabilities(&amp;caps);
    if (caps &amp; WMDM_DEVICECAP_CANPLAY)
    {
        // TODO: Display a message indicating that the media device can play MP3 audio.
    }
    if (caps &amp; WMDM_DEVICECAP_CANSTREAMPLAY)
    {
        // TODO: Display a message that the device can play audio directly from the host computer.
    }
    if (caps &amp; WMDM_DEVICECAP_CANRECORD)
    {
        // TODO: Display a message that the device can record audio.
    }
    if (caps &amp; WMDM_DEVICECAP_CANSTREAMRECORD)
    {
        // TODO: Display a message that the media device can record 
        // streaming audio directly to the host computer.
    }
    if (caps &amp; WMDM_DEVICECAP_CANPAUSE)
    {
        // TODO: Display a message that the device can pause during play or record operations.
    }
    if (caps &amp; WMDM_DEVICECAP_CANRESUME)
    {
        // TODO: Display a message that the device can resume an operation that was paused.
    }
    if (caps &amp; WMDM_DEVICECAP_CANSTOP)
    {
        // TODO: Display a message that the device can stop playing before the end of a file.
    }
    if (caps &amp; WMDM_DEVICECAP_CANSEEK)
    {
        // TODO: Display a message that the device can seek to a position 
        // other than the beginning of the file.
    }
    if (caps &amp; WMDM_DEVICECAP_HASSECURECLOCK)
    {
        // TODO: Display a message indicating that the device has a secure clock.
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 


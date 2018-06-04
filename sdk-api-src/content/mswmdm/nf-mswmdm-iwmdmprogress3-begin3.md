---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMDMProgress3::Begin3


## -description



The <b>Begin3</b> method is called by Windows Media Device Manager to indicate that an operation is about to begin. An estimate of the duration of the operation is provided when possible. This method extends <a href="https://msdn.microsoft.com/207b7cb5-4471-4be9-8252-9d467d67d7a2">IWMDMProgress::Begin</a> by providing additional input parameters for the identification (ID) of the event and for a pointer to the optional context of the commands. The operation is identified by an event ID. The method allows the caller to pass an opaque data structure to the application.




## -parameters




### -param EventId [in]

A <b>GUID</b> identifying the operation that will begin. Possible values are shown in the following table.

<table>
<tr>
<th>
                  Event
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>SCP_EVENTID_ACQSECURECLOCK</td>
<td>Windows Media Device Manager is acquiring a secure clock from server.</td>
</tr>
<tr>
<td>SCP_EVENTID_NEEDTOINDIV</td>
<td>The device is being individualized. This is not currently used.</td>
</tr>
<tr>
<td>SCP_EVENTID_DRMINFO</td>
<td>
This event ID is used to notify the application with the version DRM header found in the content for each file.

The OPAQUECOMMAND structure returned has the <b>guidCommand</b> member set to SCP_PARAMID_DRMVERSION.

In addition, the OPAQUECOMMAND specifies one of the following flags:

WMDM_SCP_DRMINFO_NOT_DRMPROTECTED

WMDM_SCP_DRMINFO_V1HEADER

WMDM_SCP_DRMINFO_V2HEADER

</td>
</tr>
<tr>
<td>EVENT_WMDM_CONTENT_TRANSFER</td>
<td>Content is being transferred to or from the device.</td>
</tr>
</table>
 


### -param dwEstimatedTicks [in]

<b>DWORD</b> specifying the estimated number of ticks that are needed for the operation to complete. The number of ticks passed in <i>dwEstimatedTicks</i> is an estimate of how many ticks are needed for the operation to complete. During the course of the operation, the <b>Progress3</b> method is called to indicate how many ticks have transpired. Applications can use the estimate to configure display mechanisms that show progress.


### -param pContext [in, out]

Pointer to an <a href="https://msdn.microsoft.com/5b39cf07-2816-4615-a754-e3f0c57bf4ce">OPAQUECOMMAND</a> structure containing a command sent to the device without being handled by Windows Media Device Manager. This parameter is optional and can be <b>NULL</b>.


## -returns



The application should return one of the following <b>HRESULT</b> values.

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
The operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager should cancel the current operation without waiting for it to finish. If the application is using block mode, then Windows Media Device Manager will return this error to the application.

</td>
</tr>
</table>
 




## -remarks



The application returns S_OK to indicate that an operation should be continued and WMDM_E_USER_CANCELLED to indicate that the operation should be cancelled. If the application is using block mode and returns WMDM_E_USER_CANCELLED, then Windows Media Device Manager will return this same error to the application.


#### Examples

The following C++ code shows an example implementation of <b>Begin3</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Begin3(GUID  EventId, DWORD  dwEstimatedTicks, OPAQUECOMMAND*  pContext)
{
    WCHAR strGuid[64];
    StringFromGUID2(reinterpret_cast&lt;GUID&amp;&gt;(EventId),(LPOLESTR)strGuid, 64);
    // TODO: Display the message "IWMDMProgress3::Begin3 called." 
    // followed by the strGuid value.
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/fc3a7031-ac1b-45cf-889b-2d40d50b347d">IWMDMProgress3 Interface</a>



<a href="https://msdn.microsoft.com/207b7cb5-4471-4be9-8252-9d467d67d7a2">IWMDMProgress::Begin</a>
 

 


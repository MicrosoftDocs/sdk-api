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

# IPortableDeviceService::SendCommand


## -description


The <b>SendCommand</b> method sends a standard WPD command and its parameters to the service.


## -parameters




### -param dwFlags [in]

Not used.


### -param pParameters [in]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface specifying the command parameters.


### -param ppResults [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface specifying the command results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



This method should only be used to send standard WPD commands to the service. To invoke service methods, use the <a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods</a> interface.

This method may fail even though it returns <b>S_OK</b> as its <b>HRESULT</b> value. To determine if a command succeeded, an application should always examine the properties referenced by the <i>ppResults</i> parameter:

<ul>
<li>The <a href="common_properties.htm">WPD_PROPERTY_COMMON_HRESULT</a> property indicates if the command succeeded.</li>
<li>If the command failed, the <a href="common_properties.htm">WPD_PROPERTY_COMMON_DRIVER_ERROR_CODE</a> property will contain driver-specific error codes.</li>
</ul>
The object referenced by the <i>pParameters</i> parameter must specify at least these properties:

<ul>
<li><a href="common_properties.htm">WPD_PROPERTY_COMMON_COMMAND_CATEGORY</a>, which should contain a command category, such as the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597754">WPD_COMMAND_COMMON_RESET_DEVICE</a> property</li>
<li><a href="common_properties.htm">WPD_PROPERTY_COMMON_COMMAND_ID</a>, which should contain a command identifier, such as the <b>pid</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff597754">WPD_COMMAND_COMMON_RESET_DEVICE</a> property.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 


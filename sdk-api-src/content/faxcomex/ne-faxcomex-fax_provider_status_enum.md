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

# FAX_PROVIDER_STATUS_ENUM enumeration


## -description


The <b>FAX_PROVIDER_STATUS_ENUM</b> enumeration defines the status values for a fax extension (a fax service provider (FSP) or a fax inbound routing extension).


## -enum-fields




### -field fpsSUCCESS

The extension loaded, linked, and initialized successfully.


### -field fpsSERVER_ERROR

A server-related error occurred while the fax service was trying to load, link, and initialize the extension; for example, there may have been insufficient memory resources. Call the <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.


### -field fpsBAD_GUID

An error occurred while the fax service was parsing the extension's installation data; the extension's GUID is invalid. Refer to the <b>InitErrorCode</b> property to get the error code. 


### -field fpsBAD_VERSION

An error occurred while the fax service was parsing the extension's installation data; the extension reports an invalid version of the FSP or routing extension API; the routing extension is the non-default MS routing extension for a desktop computer installation. Call the <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.


### -field fpsCANT_LOAD

An error occurred while the fax service was loading the FSP or routing extension's DLL. Call the <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.


### -field fpsCANT_LINK

An error occurred when the fax service attempted to dynamically link to one of the functions that the FSP or routing extension's DLL must export. Call the <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.


### -field fpsCANT_INIT

An error occurred when the fax service called the extension's initialization function. For virtual devices, the <b>InitErrorCode</b> property is an <b>HRESULT</b> value; otherwise, it is a Win32 error code. Call the <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.


## -see-also




<a href="https://msdn.microsoft.com/9378fc8c-6667-405e-adaf-bb2b1aca96ee">IFaxDeviceProvider::get_Status</a>



<a href="https://msdn.microsoft.com/496b2216-8ec6-4de9-8829-13b8ec404514">IFaxInboundRoutingExtension::get_Status</a>
 

 


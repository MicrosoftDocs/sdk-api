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

# IFaxDeviceProvider::get_Status


## -description


The <b>IFaxDeviceProvider::get_Status</b> property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.

This property is read-only.


## -parameters


## -remarks



If the FSP did not load successfully, the property indicates the reason for the failure, and <a href="https://msdn.microsoft.com/bbb2f8f1-81dd-4f54-ac91-1101ad2803fb">IFaxDeviceProvider::get_InitErrorCode</a> holds the last error code value. For more information, see <a href="https://msdn.microsoft.com/e39bbe9b-117e-4d1f-9eda-25368923f832">FAX_PROVIDER_STATUS_ENUM</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef32eb3d-e158-4740-82f5-661d5eded88c">FaxDeviceProvider</a>



<a href="https://msdn.microsoft.com/91899618-9164-4db4-94d3-a971db9f1ca0">IFaxDeviceProvider</a>



<a href="https://msdn.microsoft.com/422003a1-7db2-4eff-97bd-8ca889a3e5f6">Visual Basic Example</a>
 

 


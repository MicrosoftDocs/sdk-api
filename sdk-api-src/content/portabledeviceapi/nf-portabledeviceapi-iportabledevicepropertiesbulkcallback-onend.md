---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnEnd
title: IPortableDevicePropertiesBulkCallback::OnEnd
author: windows-sdk-content
description: The OnEnd method is called by the SDK when a bulk operation that is started by IPortableDevicePropertiesBulk::Start is completed.
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onend.htm
old-project: wpd_sdk
ms.assetid: a3e56415-fe75-4d54-8448-6ca7793147fd
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],OnEnd method, IPortableDevicePropertiesBulkCallback.OnEnd, IPortableDevicePropertiesBulkCallback::OnEnd, IPortableDevicePropertiesBulkCallbackOnEnd, OnEnd, OnEnd method [Windows Portable Devices SDK], OnEnd method [Windows Portable Devices SDK],IPortableDevicePropertiesBulkCallback interface, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnEnd, wpdsdk.iportabledevicepropertiesbulkcallback_onend
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
-	IPortableDevicePropertiesBulkCallback.OnEnd
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDevicePropertiesBulkCallback::OnEnd


## -description



The <b>OnEnd</b> method is called by the SDK when a bulk operation that is started by <a href="https://msdn.microsoft.com/a69afdc9-622d-45fc-b71e-6058d9d528b0">IPortableDevicePropertiesBulk::Start</a> is completed.




## -parameters




### -param pContext [in]

Pointer to a GUID that identifies which operation has finished. This value is produced by a <b>Queue</b>... method of the <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk</a> interface.


### -param hrStatus [out]

Contains any errors returned by the driver after the bulk operation has completed.


## -returns



The method's return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback Interface</a>
 

 


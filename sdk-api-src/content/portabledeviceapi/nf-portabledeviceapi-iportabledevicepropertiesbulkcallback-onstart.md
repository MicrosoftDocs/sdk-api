---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnStart
title: IPortableDevicePropertiesBulkCallback::OnStart method
author: windows-driver-content
description: The OnStart method is called by the SDK when a bulk operation started by IPortableDevicePropertiesBulk::Start is about to begin.
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onstart.htm
old-project: wpd_sdk
ms.assetid: bde04e04-d36e-4471-b598-ee38dba9f614
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IPortableDevicePropertiesBulkCallback, IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK], OnStart method, IPortableDevicePropertiesBulkCallback::OnStart, IPortableDevicePropertiesBulkCallbackOnStart, OnStart method [Windows Portable Devices SDK], OnStart method [Windows Portable Devices SDK], IPortableDevicePropertiesBulkCallback interface, OnStart,IPortableDevicePropertiesBulkCallback.OnStart, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnStart, wpdsdk.iportabledevicepropertiesbulkcallback_onstart
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
-	IPortableDevicePropertiesBulkCallback.OnStart
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDevicePropertiesBulkCallback::OnStart method


## -description



The <b>OnStart</b> method is called by the SDK when a bulk operation started by <a href="https://msdn.microsoft.com/a69afdc9-622d-45fc-b71e-6058d9d528b0">IPortableDevicePropertiesBulk::Start</a> is about to begin.




## -parameters




### -param pContext [in]

Pointer to a GUID that identifies which operation has started. This value is produced by a <b>Queue</b>... method of the <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk</a> interface.


## -returns



The application should return either S_OK or an error code to abandon the operation. The application should handle all error codes in the same manner.




## -see-also




<a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback Interface</a>
 

 


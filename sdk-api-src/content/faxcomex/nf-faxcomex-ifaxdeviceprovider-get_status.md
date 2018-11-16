---
UID: NF:faxcomex.IFaxDeviceProvider.get_Status
title: IFaxDeviceProvider::get_Status
author: windows-sdk-content
description: The IFaxDeviceProvider::get_Status property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.
old-location: fax\_mfax_faxdeviceprovider_status.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_8joz.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDeviceProvider interface [Fax Service],Status property, IFaxDeviceProvider.Status, IFaxDeviceProvider.get_Status, IFaxDeviceProvider::Status, IFaxDeviceProvider::get_Status, Status property [Fax Service], Status property [Fax Service],IFaxDeviceProvider interface, _mfax_faxdeviceprovider.status, fax._mfax_faxdeviceprovider_status, faxcomex/IFaxDeviceProvider::Status, faxcomex/IFaxDeviceProvider::get_Status, get_Status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDeviceProvider.Status
 - IFaxDeviceProvider.get_Status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxDeviceProvider.get_Status
: 
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
 

 


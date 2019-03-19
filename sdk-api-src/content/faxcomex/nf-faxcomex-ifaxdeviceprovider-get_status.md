---
UID: NF:faxcomex.IFaxDeviceProvider.get_Status
title: IFaxDeviceProvider::get_Status (faxcomex.h)
author: windows-sdk-content
description: The IFaxDeviceProvider::get_Status property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.
old-location: fax\_mfax_faxdeviceprovider_status.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_8joz.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDeviceProvider interface [Fax Service],Status property, IFaxDeviceProvider.Status, IFaxDeviceProvider.get_Status, IFaxDeviceProvider::Status, IFaxDeviceProvider::get_Status, Status property [Fax Service], Status property [Fax Service],IFaxDeviceProvider interface, _mfax_faxdeviceprovider.status, fax._mfax_faxdeviceprovider_status, faxcomex/IFaxDeviceProvider::Status, faxcomex/IFaxDeviceProvider::get_Status, get_Status
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
---

# IFaxDeviceProvider::get_Status


## -description


The <b>IFaxDeviceProvider::get_Status</b> property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.

This property is read-only.


## -parameters


## -remarks



If the FSP did not load successfully, the property indicates the reason for the failure, and <a href="https://msdn.microsoft.com/en-us/library/ms684578(v=VS.85).aspx">IFaxDeviceProvider::get_InitErrorCode</a> holds the last error code value. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690089(v=VS.85).aspx">FAX_PROVIDER_STATUS_ENUM</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684890(v=VS.85).aspx">FaxDeviceProvider</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684893(v=VS.85).aspx">IFaxDeviceProvider</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693462(v=VS.85).aspx">Visual Basic Example</a>
 

 


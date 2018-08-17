---
UID: NF:winddi.DrvDisableDriver
title: DrvDisableDriver function
author: windows-sdk-content
description: The DrvDisableDriver function is used by GDI to notify a driver that it no longer requires the driver and is ready to unload it.
old-location: display\drvdisabledriver.htm
old-project: display
ms.assetid: 8f12cc40-6cff-4e40-a264-58d16d3e55bd
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DrvDisableDriver, DrvDisableDriver function [Display Devices], ddifncs_213ec824-0230-4b4b-879e-ed48401f3788.xml, display.drvdisabledriver, winddi/DrvDisableDriver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDisableDriver
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvDisableDriver function


## -description


The <b>DrvDisableDriver</b> function is used by GDI to notify a driver that it no longer requires the driver and is ready to unload it.


## -parameters






## -returns



None




## -remarks



The driver should free all allocated resources and return the device to the state it was in before the driver was loaded.

<b>DrvDisableDriver</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/b7aa5442-bbf5-4f9e-ad39-bf8a2d01c50e">DrvEnableDriver</a>
 

 


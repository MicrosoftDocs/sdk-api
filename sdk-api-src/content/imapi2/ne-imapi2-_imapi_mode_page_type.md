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

# _IMAPI_MODE_PAGE_TYPE enumeration


## -description


Defines values for the mode pages that are supported by CD and DVD devices.  


## -enum-fields




### -field IMAPI_MODE_PAGE_TYPE_READ_WRITE_ERROR_RECOVERY

The mode page specifies the error recovery parameters the
drive uses during any command that performs a data read or write operation from the media.


### -field IMAPI_MODE_PAGE_TYPE_MRW

The mode page provides a method by which the host may control the special features of a
MRW CD-RW Drive.


### -field IMAPI_MODE_PAGE_TYPE_WRITE_PARAMETERS

The mode page provides parameters that are often needed in the execution of
commands that write to the media.


### -field IMAPI_MODE_PAGE_TYPE_CACHING

The mode page contains parameters to enable or disable caching during read or write operations.


### -field IMAPI_MODE_PAGE_TYPE_INFORMATIONAL_EXCEPTIONS

The mode page contains parameters for exception reporting mechanisms that result in specific sense code errors when failures are predicted.  This mode page is related to the <a href="https://msdn.microsoft.com/659ed2c9-7c58-4030-be41-273e597d6f1f">S.M.A.R.T.</a> feature.


### -field IMAPI_MODE_PAGE_TYPE_TIMEOUT_AND_PROTECT

The mode page contains command time-out values that are  suggested by the device.


### -field IMAPI_MODE_PAGE_TYPE_POWER_CONDITION

The mode page contains power management settings for the drive. The parameters define how long the logical unit delays before changing its internal power state.


### -field IMAPI_MODE_PAGE_TYPE_LEGACY_CAPABILITIES

The mode page contains legacy device capabilities. These are superseded by the feature pages returned through the GetConfiguration command.


## -remarks



Note that the range of mode page type values is 0x0000 to 0xFFFF. This enumeration contains those features defined in the Multmedia Commands - 5 (MMC) specification. For a complete definition of each feature, see Mode Parameters for Multi-Media Devices in the latest release of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a6fe1c3-7ce2-4877-93e6-de4ab87685a0">IDiscRecorder2::get_SupportedModePages</a>



<a href="https://msdn.microsoft.com/69e163a6-943d-4626-8120-778c9ca1777f">IDiscRecorder2Ex::GetModePage</a>



<a href="https://msdn.microsoft.com/343d976e-97f3-4231-a417-4ebe7967f99c">IDiscRecorder2Ex::GetSupportedModePages</a>
 

 


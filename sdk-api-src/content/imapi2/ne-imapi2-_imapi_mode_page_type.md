---
UID: NE:imapi2._IMAPI_MODE_PAGE_TYPE
title: "_IMAPI_MODE_PAGE_TYPE"
author: windows-sdk-content
description: Defines values for the mode pages that are supported by CD and DVD devices.
old-location: imapi\imapi_mode_page_type.htm
old-project: imapi
ms.assetid: da6262a0-2b21-4568-9da1-dc8ca1ba2b4a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PIMAPI_MODE_PAGE_TYPE, IMAPI_MODE_PAGE_TYPE, IMAPI_MODE_PAGE_TYPE enumeration [IMAPI], IMAPI_MODE_PAGE_TYPE_CACHING, IMAPI_MODE_PAGE_TYPE_INFORMATIONAL_EXCEPTIONS, IMAPI_MODE_PAGE_TYPE_LEGACY_CAPABILITIES, IMAPI_MODE_PAGE_TYPE_MRW, IMAPI_MODE_PAGE_TYPE_POWER_CONDITION, IMAPI_MODE_PAGE_TYPE_READ_WRITE_ERROR_RECOVERY, IMAPI_MODE_PAGE_TYPE_TIMEOUT_AND_PROTECT, IMAPI_MODE_PAGE_TYPE_WRITE_PARAMETERS, PIMAPI_MODE_PAGE_TYPE, PIMAPI_MODE_PAGE_TYPE enumeration pointer [IMAPI], _IMAPI_MODE_PAGE_TYPE, imapi.imapi_mode_page_type, imapi2/IMAPI_MODE_PAGE_TYPE, imapi2/IMAPI_MODE_PAGE_TYPE_CACHING, imapi2/IMAPI_MODE_PAGE_TYPE_INFORMATIONAL_EXCEPTIONS, imapi2/IMAPI_MODE_PAGE_TYPE_LEGACY_CAPABILITIES, imapi2/IMAPI_MODE_PAGE_TYPE_MRW, imapi2/IMAPI_MODE_PAGE_TYPE_POWER_CONDITION, imapi2/IMAPI_MODE_PAGE_TYPE_READ_WRITE_ERROR_RECOVERY, imapi2/IMAPI_MODE_PAGE_TYPE_TIMEOUT_AND_PROTECT, imapi2/IMAPI_MODE_PAGE_TYPE_WRITE_PARAMETERS, imapi2/PIMAPI_MODE_PAGE_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_MODE_PAGE_TYPE, *PIMAPI_MODE_PAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2.h
api_name:
 - IMAPI_MODE_PAGE_TYPE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 


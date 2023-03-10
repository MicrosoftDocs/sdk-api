---
UID: NE:imapi2._IMAPI_MODE_PAGE_REQUEST_TYPE
title: IMAPI_MODE_PAGE_REQUEST_TYPE (imapi2.h)
description: Defines values that indicate requests sent to a device using the MODE_SENSE10 MMC command.
helpviewer_keywords: ["*PIMAPI_MODE_PAGE_REQUEST_TYPE","IMAPI_MODE_PAGE_REQUEST_TYPE","IMAPI_MODE_PAGE_REQUEST_TYPE enumeration [IMAPI]","IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES","IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES","IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES","IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES","PIMAPI_MODE_PAGE_REQUEST_TYPE","PIMAPI_MODE_PAGE_REQUEST_TYPE enumeration pointer [IMAPI]","imapi.imapi_mode_page_request_type","imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE","imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES","imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES","imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES","imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES","imapi2/PIMAPI_MODE_PAGE_REQUEST_TYPE"]
old-location: imapi\imapi_mode_page_request_type.htm
tech.root: imapi
ms.assetid: f27cd003-34a0-4aee-81d5-74fb02d9427c
ms.date: 12/05/2018
ms.keywords: '*PIMAPI_MODE_PAGE_REQUEST_TYPE, IMAPI_MODE_PAGE_REQUEST_TYPE, IMAPI_MODE_PAGE_REQUEST_TYPE enumeration [IMAPI], IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES, IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES, IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES, IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES, PIMAPI_MODE_PAGE_REQUEST_TYPE, PIMAPI_MODE_PAGE_REQUEST_TYPE enumeration pointer [IMAPI], imapi.imapi_mode_page_request_type, imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE, imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES, imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES, imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES, imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES, imapi2/PIMAPI_MODE_PAGE_REQUEST_TYPE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAPI_MODE_PAGE_REQUEST_TYPE, *PIMAPI_MODE_PAGE_REQUEST_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAPI_MODE_PAGE_REQUEST_TYPE
 - imapi2/_IMAPI_MODE_PAGE_REQUEST_TYPE
 - PIMAPI_MODE_PAGE_REQUEST_TYPE
 - imapi2/PIMAPI_MODE_PAGE_REQUEST_TYPE
 - IMAPI_MODE_PAGE_REQUEST_TYPE
 - imapi2/IMAPI_MODE_PAGE_REQUEST_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2.h
api_name:
 - IMAPI_MODE_PAGE_REQUEST_TYPE
---

# IMAPI_MODE_PAGE_REQUEST_TYPE enumeration


## -description

Defines values that indicate requests sent to a device using the MODE_SENSE10 MMC command.

## -enum-fields

### -field IMAPI_MODE_PAGE_REQUEST_TYPE_CURRENT_VALUES:0

Requests current settings of the mode page.  This is the most common request type, and the most commonly supported type of this command.

### -field IMAPI_MODE_PAGE_REQUEST_TYPE_CHANGEABLE_VALUES:1

Requests a mask that indicates settings that are write enabled. A write-enabled setting has a corresponding bit that is set to one in the mask. A read-only setting has a corresponding bit that is set to zero in the mask .

### -field IMAPI_MODE_PAGE_REQUEST_TYPE_DEFAULT_VALUES:2

Requests the power-on settings of the drive.

### -field IMAPI_MODE_PAGE_REQUEST_TYPE_SAVED_VALUES:3

Requests a saved configuration for a drive. This functionality might not be supported on all devices.


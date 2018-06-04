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

# __MIDL___MIDL_itf_tpmvscmgr_0000_0000_0002 enumeration


## -description


Provides predefined error codes to represent the contexts of errors from the TPM virtual smart card manager.


## -enum-fields




### -field TPMVSCMGR_ERROR_IMPERSONATION

Failed to impersonate the caller.


### -field TPMVSCMGR_ERROR_PIN_COMPLEXITY

Ensure that your PIN/PUK meets the length or complexity requirements of your organization.


### -field TPMVSCMGR_ERROR_READER_COUNT_LIMIT

The limit of the number of smart card readers has been reached.


### -field TPMVSCMGR_ERROR_TERMINAL_SERVICES_SESSION

TPM virtual smart card management cannot be used within a Terminal Services session.


### -field TPMVSCMGR_ERROR_VTPMSMARTCARD_INITIALIZE

Failed to initialize the virtual smart card manager.


### -field TPMVSCMGR_ERROR_VTPMSMARTCARD_CREATE

Failed to create the virtual smart card manager.


### -field TPMVSCMGR_ERROR_VTPMSMARTCARD_DESTROY

Failed to destroy the virtual smart card manager.


### -field TPMVSCMGR_ERROR_VGIDSSIMULATOR_INITIALIZE

Failed to initialize the virtual smart card simulator.


### -field TPMVSCMGR_ERROR_VGIDSSIMULATOR_CREATE

Failed to create the virtual smart card simulator.


### -field TPMVSCMGR_ERROR_VGIDSSIMULATOR_DESTROY

Failed to destroy the virtual smart card simulator.


### -field TPMVSCMGR_ERROR_VGIDSSIMULATOR_WRITE_PROPERTY

Failed to configure the virtual smart card simulator.


### -field TPMVSCMGR_ERROR_VGIDSSIMULATOR_READ_PROPERTY

Failed to find the specified virtual smart card simulator.


### -field TPMVSCMGR_ERROR_VREADER_INITIALIZE

Failed to initialize the virtual smart card reader.


### -field TPMVSCMGR_ERROR_VREADER_CREATE

Failed to create the virtual smart card reader.


### -field TPMVSCMGR_ERROR_VREADER_DESTROY

Failed to destroy the virtual smart card reader.


### -field TPMVSCMGR_ERROR_GENERATE_LOCATE_READER

Failed to connect to the TPM smart card.


### -field TPMVSCMGR_ERROR_GENERATE_FILESYSTEM

Failed to generate the file system on the TPM smart card.


### -field TPMVSCMGR_ERROR_CARD_CREATE

Unable to create the TPM smart card.


### -field TPMVSCMGR_ERROR_CARD_DESTROY

Unable to destroy the TPM smart card.


## -remarks



These error codes are sent from the TPM virtual smart card manager COM server to the caller through the status callback interface, <a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a>. Status callback interface implementations must interpret the error codes based on their predefined meanings and, if applicable, load localized message strings and update the user interface.




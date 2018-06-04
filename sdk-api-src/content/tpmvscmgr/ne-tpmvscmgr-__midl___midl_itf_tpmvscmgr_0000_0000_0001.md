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

# __MIDL___MIDL_itf_tpmvscmgr_0000_0000_0001 enumeration


## -description


Provides predefined status codes to represent the progress of the TPM virtual smart card manager.


## -enum-fields




### -field TPMVSCMGR_STATUS_VTPMSMARTCARD_INITIALIZING

Initializing the virtual smart card 	manager.


### -field TPMVSCMGR_STATUS_VTPMSMARTCARD_CREATING

Creating the virtual smart card manager.


### -field TPMVSCMGR_STATUS_VTPMSMARTCARD_DESTROYING

Destroying the virtual smart card manager.


### -field TPMVSCMGR_STATUS_VGIDSSIMULATOR_INITIALIZING

Initializing  the virtual smart card simulator.


### -field TPMVSCMGR_STATUS_VGIDSSIMULATOR_CREATING

Creating the virtual smart card simulator.


### -field TPMVSCMGR_STATUS_VGIDSSIMULATOR_DESTROYING

Destroying the virtual smart card simulator.


### -field TPMVSCMGR_STATUS_VREADER_INITIALIZING

Initializing the virtual smart card reader.


### -field TPMVSCMGR_STATUS_VREADER_CREATING

Creating the virtual smart card reader.


### -field TPMVSCMGR_STATUS_VREADER_DESTROYING

Destroying the virtual smart card reader.


### -field TPMVSCMGR_STATUS_GENERATE_WAITING

Waiting for the TPM smart card device.


### -field TPMVSCMGR_STATUS_GENERATE_AUTHENTICATING

Authenticating to the TPM smart card.


### -field TPMVSCMGR_STATUS_GENERATE_RUNNING

Generating the file system on the TPM smart card.


### -field TPMVSCMGR_STATUS_CARD_CREATED

Creation of the TPM smart card  is complete.


### -field TPMVSCMGR_STATUS_CARD_DESTROYED

Destruction of the TPM smart card is complete.


## -remarks



These status codes are sent from the TPM virtual smart card manager COM server to the caller through the status callback interface, <a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a>. Status callback interface implementations must interpret the status codes based on their predefined meanings and, if applicable, load localized message strings and update the user interface.




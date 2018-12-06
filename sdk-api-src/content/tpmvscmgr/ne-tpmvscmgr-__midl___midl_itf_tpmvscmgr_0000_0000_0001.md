---
UID: NE:tpmvscmgr.__MIDL___MIDL_itf_tpmvscmgr_0000_0000_0001
title: "__MIDL___MIDL_itf_tpmvscmgr_0000_0000_0001"
author: windows-sdk-content
description: Provides predefined status codes to represent the progress of the TPM virtual smart card manager.
old-location: security\tpmvscmgr_status.htm
tech.root: secauthn
ms.assetid: 9E678584-D225-4BDD-8035-92818B977DE9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TPMVSCMGR_STATUS, TPMVSCMGR_STATUS enumeration [Security], TPMVSCMGR_STATUS_CARD_CREATED, TPMVSCMGR_STATUS_CARD_DESTROYED, TPMVSCMGR_STATUS_GENERATE_AUTHENTICATING, TPMVSCMGR_STATUS_GENERATE_RUNNING, TPMVSCMGR_STATUS_GENERATE_WAITING, TPMVSCMGR_STATUS_VGIDSSIMULATOR_CREATING, TPMVSCMGR_STATUS_VGIDSSIMULATOR_DESTROYING, TPMVSCMGR_STATUS_VGIDSSIMULATOR_INITIALIZING, TPMVSCMGR_STATUS_VREADER_CREATING, TPMVSCMGR_STATUS_VREADER_DESTROYING, TPMVSCMGR_STATUS_VREADER_INITIALIZING, TPMVSCMGR_STATUS_VTPMSMARTCARD_CREATING, TPMVSCMGR_STATUS_VTPMSMARTCARD_DESTROYING, TPMVSCMGR_STATUS_VTPMSMARTCARD_INITIALIZING, __MIDL___MIDL_itf_tpmvscmgr_0000_0000_0001, security.tpmvscmgr_status, tpmvscmgr/TPMVSCMGR_STATUS, tpmvscmgr/TPMVSCMGR_STATUS_CARD_CREATED, tpmvscmgr/TPMVSCMGR_STATUS_CARD_DESTROYED, tpmvscmgr/TPMVSCMGR_STATUS_GENERATE_AUTHENTICATING, tpmvscmgr/TPMVSCMGR_STATUS_GENERATE_RUNNING, tpmvscmgr/TPMVSCMGR_STATUS_GENERATE_WAITING, tpmvscmgr/TPMVSCMGR_STATUS_VGIDSSIMULATOR_CREATING, tpmvscmgr/TPMVSCMGR_STATUS_VGIDSSIMULATOR_DESTROYING, tpmvscmgr/TPMVSCMGR_STATUS_VGIDSSIMULATOR_INITIALIZING, tpmvscmgr/TPMVSCMGR_STATUS_VREADER_CREATING, tpmvscmgr/TPMVSCMGR_STATUS_VREADER_DESTROYING, tpmvscmgr/TPMVSCMGR_STATUS_VREADER_INITIALIZING, tpmvscmgr/TPMVSCMGR_STATUS_VTPMSMARTCARD_CREATING, tpmvscmgr/TPMVSCMGR_STATUS_VTPMSMARTCARD_DESTROYING, tpmvscmgr/TPMVSCMGR_STATUS_VTPMSMARTCARD_INITIALIZING
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tpmvscmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tpmvscmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Vscmgr.lib
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Vscmgr.lib
api_name:
 - TPMVSCMGR_STATUS
product: Windows
targetos: Windows
req.typenames: TPMVSCMGR_STATUS
req.redist: 
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




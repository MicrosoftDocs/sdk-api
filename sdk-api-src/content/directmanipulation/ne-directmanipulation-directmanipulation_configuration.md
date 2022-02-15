---
UID: NE:directmanipulation.DIRECTMANIPULATION_CONFIGURATION
title: DIRECTMANIPULATION_CONFIGURATION (directmanipulation.h)
description: Defines the interaction configuration states available in Direct Manipulation.
helpviewer_keywords: ["DIRECTMANIPULATION_CONFIGURATION","DIRECTMANIPULATION_CONFIGURATION enumeration [Direct Manipulation]","DIRECTMANIPULATION_CONFIGURATION_INTERACTION","DIRECTMANIPULATION_CONFIGURATION_NONE","DIRECTMANIPULATION_CONFIGURATION_RAILS_X","DIRECTMANIPULATION_CONFIGURATION_RAILS_Y","DIRECTMANIPULATION_CONFIGURATION_SCALING","DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA","DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA","DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X","DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y","directmanipulation.directmanipulation_configuration","directmanipulation/DIRECTMANIPULATION_CONFIGURATION","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_INTERACTION","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_NONE","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_X","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_Y","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X","directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y"]
old-location: directmanipulation\directmanipulation_configuration.htm
tech.root: directmanipulation
ms.assetid: a7c146e8-a1df-4445-8230-1dd491d0e9a3
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_CONFIGURATION, DIRECTMANIPULATION_CONFIGURATION enumeration [Direct Manipulation], DIRECTMANIPULATION_CONFIGURATION_INTERACTION, DIRECTMANIPULATION_CONFIGURATION_NONE, DIRECTMANIPULATION_CONFIGURATION_RAILS_X, DIRECTMANIPULATION_CONFIGURATION_RAILS_Y, DIRECTMANIPULATION_CONFIGURATION_SCALING, DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X, DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y, directmanipulation.directmanipulation_configuration, directmanipulation/DIRECTMANIPULATION_CONFIGURATION, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_INTERACTION, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_NONE, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_X, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_RAILS_Y, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X, directmanipulation/DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIRECTMANIPULATION_CONFIGURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_CONFIGURATION
 - directmanipulation/DIRECTMANIPULATION_CONFIGURATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_CONFIGURATION
---

# DIRECTMANIPULATION_CONFIGURATION enumeration


## -description

Defines the interaction configuration states available in <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

## -enum-fields

### -field DIRECTMANIPULATION_CONFIGURATION_NONE:0

No interaction is defined.

### -field DIRECTMANIPULATION_CONFIGURATION_INTERACTION:0x1

An interaction is defined. To enable interactions, this value must be included.

Required when setting a configuration other than <b>DIRECTMANIPULATION_CONFIGURATION_NONE</b>.

### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X:0x2

Translation in the horizontal axis.

### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y:0x4

Translation in the vertical axis.

### -field DIRECTMANIPULATION_CONFIGURATION_SCALING:0x10

Zoom.

### -field DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_INERTIA:0x20

Inertia for translation as defined by <b>DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X</b> and <b>DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_Y</b>.

### -field DIRECTMANIPULATION_CONFIGURATION_SCALING_INERTIA:0x80

Inertia for zoom as defined by <b>DIRECTMANIPULATION_CONFIGURATION _SCALING</b>.

### -field DIRECTMANIPULATION_CONFIGURATION_RAILS_X:0x100

Rails on the horizontal axis.

### -field DIRECTMANIPULATION_CONFIGURATION_RAILS_Y:0x200

Rails on the vertical axis.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>



<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>

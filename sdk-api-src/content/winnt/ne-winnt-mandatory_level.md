---
UID: NE:winnt._MANDATORY_LEVEL
title: MANDATORY_LEVEL (winnt.h)
description: Lists the possible security levels.
helpviewer_keywords: ["*PMANDATORY_LEVEL","MANDATORY_LEVEL","MANDATORY_LEVEL enumeration [Security]","MandatoryLevelCount","MandatoryLevelHigh","MandatoryLevelLow","MandatoryLevelMedium","MandatoryLevelSecureProcess","MandatoryLevelSystem","MandatoryLevelUntrusted","security.mandatory_level","winnt/MANDATORY_LEVEL","winnt/MandatoryLevelCount","winnt/MandatoryLevelHigh","winnt/MandatoryLevelLow","winnt/MandatoryLevelMedium","winnt/MandatoryLevelSecureProcess","winnt/MandatoryLevelSystem","winnt/MandatoryLevelUntrusted"]
old-location: security\mandatory_level.htm
tech.root: security
ms.assetid: 0D6EC16C-F21E-4BED-AF57-93D282D6CF86
ms.date: 12/05/2018
ms.keywords: '*PMANDATORY_LEVEL, MANDATORY_LEVEL, MANDATORY_LEVEL enumeration [Security], MandatoryLevelCount, MandatoryLevelHigh, MandatoryLevelLow, MandatoryLevelMedium, MandatoryLevelSecureProcess, MandatoryLevelSystem, MandatoryLevelUntrusted, security.mandatory_level, winnt/MANDATORY_LEVEL, winnt/MandatoryLevelCount, winnt/MandatoryLevelHigh, winnt/MandatoryLevelLow, winnt/MandatoryLevelMedium, winnt/MandatoryLevelSecureProcess, winnt/MandatoryLevelSystem, winnt/MandatoryLevelUntrusted'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MANDATORY_LEVEL, *PMANDATORY_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MANDATORY_LEVEL
 - winnt/_MANDATORY_LEVEL
 - PMANDATORY_LEVEL
 - winnt/PMANDATORY_LEVEL
 - MANDATORY_LEVEL
 - winnt/MANDATORY_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MANDATORY_LEVEL
---

# MANDATORY_LEVEL enumeration


## -description

The <b>MANDATORY_LEVEL</b> enumeration lists the possible security levels.

## -enum-fields

### -field MandatoryLevelUntrusted:0

The required security level is untrusted.

### -field MandatoryLevelLow

The required security level is low.

### -field MandatoryLevelMedium

The required security level is medium.

### -field MandatoryLevelHigh

The required security level is high.

### -field MandatoryLevelSystem

The required security level is system.

### -field MandatoryLevelSecureProcess

The required security level is a secure process.

### -field MandatoryLevelCount

The count of the mandatory level.


---
UID: NE:combaseapi.AgileReferenceOptions
title: AgileReferenceOptions (combaseapi.h)
description: Specifies options for the RoGetAgileReference function.
helpviewer_keywords: ["AGILEREFERENCE_DEFAULT","AGILEREFERENCE_DELAYEDMARSHAL","AgileReferenceOptions","AgileReferenceOptions enumeration [Windows Runtime]","combaseapi/AGILEREFERENCE_DEFAULT","combaseapi/AGILEREFERENCE_DELAYEDMARSHAL","combaseapi/AgileReferenceOptions","winrt.agilereferenceoptions"]
old-location: winrt\agilereferenceoptions.htm
tech.root: WinRT
ms.assetid: F46FD597-F278-4DA8-BC94-26836684AD7E
ms.date: 12/05/2018
ms.keywords: AGILEREFERENCE_DEFAULT, AGILEREFERENCE_DELAYEDMARSHAL, AgileReferenceOptions, AgileReferenceOptions enumeration [Windows Runtime], combaseapi/AGILEREFERENCE_DEFAULT, combaseapi/AGILEREFERENCE_DELAYEDMARSHAL, combaseapi/AgileReferenceOptions, winrt.agilereferenceoptions
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AgileReferenceOptions
 - combaseapi/AgileReferenceOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - AgileReferenceOptions
---

# AgileReferenceOptions enumeration


## -description

Specifies options for the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-rogetagilereference">RoGetAgileReference</a> function.

## -enum-fields

### -field AGILEREFERENCE_DEFAULT:0

Use the default marshaling behavior, which is to marshal interfaces when an agile reference to the interface is obtained.

### -field AGILEREFERENCE_DELAYEDMARSHAL:1

Marshaling happens on demand.  Use this option only in situations where it's known that an object is only resolved from the same apartment in which it was registered.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-rogetagilereference">RoGetAgileReference</a>

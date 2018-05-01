---
UID: NE:combaseapi.AgileReferenceOptions
title: AgileReferenceOptions
author: windows-driver-content
description: Specifies options for the RoGetAgileReference function.
old-location: winrt\agilereferenceoptions.htm
old-project: WinRT
ms.assetid: F46FD597-F278-4DA8-BC94-26836684AD7E
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: AGILEREFERENCE_DEFAULT, AGILEREFERENCE_DELAYEDMARSHAL, AgileReferenceOptions, AgileReferenceOptions enumeration [Windows Runtime], combaseapi/AGILEREFERENCE_DEFAULT, combaseapi/AGILEREFERENCE_DELAYEDMARSHAL, combaseapi/AgileReferenceOptions, winrt.agilereferenceoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	combaseapi.h
api_name:
-	AgileReferenceOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# AgileReferenceOptions enumeration


## -description


Specifies options for the <a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a> function.


## -enum-fields




### -field AGILEREFERENCE_DEFAULT

Use the default marshaling behavior, which is to marshal interfaces when an agile reference to the interface is obtained.


### -field AGILEREFERENCE_DELAYEDMARSHAL

Marshaling happens on demand.  Use this option only in situations where it's known that an object is only resolved from the same apartment in which it was registered.


## -see-also




<a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a>
 

 


---
UID: NF:wbemdisp.ISWbemProperty.get_Origin
title: ISWbemProperty::get_Origin
author: windows-sdk-content
description: The Origin property of the SWbemProperty object retrieves the name of the WMI class in which this property was introduced. For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.
old-location: wmi\swbemproperty_origin.htm
old-project: WmiSdk
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemProperty interface [Windows Management Instrumentation],Origin property, ISWbemProperty.get_Origin, ISWbemProperty::get_Origin, Origin property [Windows Management Instrumentation], Origin property [Windows Management Instrumentation],ISWbemProperty interface, Origin property [Windows Management Instrumentation],SWbemProperty object, SWbemProperty object [Windows Management Instrumentation],Origin property, SWbemProperty.Origin, _hmm_swbemproperty.origin, get_Origin, wmi.swbemproperty_origin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemProperty.Origin
 - ISWbemProperty.Origin
 - ISWbemProperty.get_Origin
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemProperty::get_Origin


## -description


The 
<b>Origin</b> property of the 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object retrieves the name of the WMI class in which this property was introduced. For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.

If the property is local (see 
<a href="https://msdn.microsoft.com/ee403bcb-894f-47b7-88cc-d354e20b4e36">SWbemQualifier.IsLocal</a>), this value is the same as the owning class. This property is read-only.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


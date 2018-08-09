---
UID: NF:wbemdisp.ISWbemProperty.get_CIMType
title: ISWbemProperty::get_CIMType
author: windows-sdk-content
description: The CIMType property of the SWbemProperty object is an integer that can be used to determine the CIM type of this property. This property is read-only.
old-location: wmi\swbemproperty_cimtype.htm
old-project: WmiSdk
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CIMType property [Windows Management Instrumentation], CIMType property [Windows Management Instrumentation],ISWbemProperty interface, CIMType property [Windows Management Instrumentation],SWbemProperty object, ISWbemProperty interface [Windows Management Instrumentation],CIMType property, ISWbemProperty.get_CIMType, ISWbemProperty::get_CIMType, SWbemProperty object [Windows Management Instrumentation],CIMType property, SWbemProperty.CIMType, _hmm_swbemproperty.cimtype, get_CIMType, wmi.swbemproperty_cimtype
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
 - SWbemProperty.CIMType
 - ISWbemProperty.CIMType
 - ISWbemProperty.get_CIMType
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemProperty::get_CIMType


## -description


The 
<b>CIMType</b> property of the 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object is an integer that can be used to determine the CIM type of this property. This property is read-only.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



For more information about valid types for this property, see 
<a href="https://msdn.microsoft.com/d9929464-742e-4f6c-b631-a6c191167858">WbemCimtypeEnum</a>.

Instances of embedded objects are stored in composite objects as properties of type <b>CIM_OBJECT</b>. To determine the class of an embedded object in an instance of a composite class, you must examine the 
<b>CIMType</b> qualifier of the <b>CIM_OBJECT</b> type property.

The object references in an association class are stored in properties of type <b>CIM_REFERENCE</b>. To determine the actual object paths you must examine the 
<b>CIMType</b> qualifier of the <b>CIM_REFERENCE</b> type property.




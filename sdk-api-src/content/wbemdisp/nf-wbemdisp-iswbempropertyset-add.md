---
UID: NF:wbemdisp.ISWbemPropertySet.Add
title: ISWbemPropertySet::Add
author: windows-sdk-content
description: The Add method of the SWbemPropertySet object adds an SWbemProperty object to the SWbemPropertySet collection. If a property with the same name already exists in the collection, its contents are replaced with the new definition.
old-location: wmi\swbempropertyset_add.htm
old-project: WmiSdk
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],ISWbemPropertySet interface, Add method [Windows Management Instrumentation],SWbemPropertySet object, ISWbemPropertySet interface [Windows Management Instrumentation],Add method, ISWbemPropertySet.Add, ISWbemPropertySet::Add, SWbemPropertySet object [Windows Management Instrumentation],Add method, SWbemPropertySet.Add, _hmm_swbempropertyset.add, wmi.swbempropertyset_add
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
 - SWbemPropertySet.Add
 - ISWbemPropertySet.Add
 - ISWbemPropertySet.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPropertySet::Add


## -description


The <b>Add</b> method of the 
    <a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> object adds an 
    <a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object to the 
    <b>SWbemPropertySet</b> collection. If a property with the same 
    name already exists in the collection, its contents are replaced with the new definition.
<div class="alert"><b>Note</b>  The value of the added property is <b>NULL</b> (unassigned) after this operation. To set 
    or change the value of a WMI property, you must set the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a> property of the returned 
    <a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object.</div><div> </div>For an explanation of this syntax, see 
    <a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the new property.


### -param iCIMType [in]

Required. An integer that represents the <b>CIMType</b> qualifier of the new 
      property. See <a href="https://msdn.microsoft.com/d9929464-742e-4f6c-b631-a6c191167858">WbemCimTypeEnum</a> for the list with the 
      <b>CIMType</b> qualifiers and their values.


### -param bIsArray [in, optional]

Specifies whether the property is an array type. The default value for this parameter is <b>FALSE</b>.


### -param iFlags [in, optional]

Reserved and must be zero if specified.


### -param objWbemProperty






## -returns



If successful, this method returns an 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object that represents the new property. Otherwise, a <b>null</b> object is returned.




## -see-also




<a href="https://msdn.microsoft.com/547ec691-ff1c-4a6d-bee8-54e73d21cc93">SWbemProperty.Value</a>



<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a>



<a href="https://msdn.microsoft.com/2a1005db-033c-48f9-8ea0-0bd43b8c989f">SWbemPropertySet.Remove</a>
 

 


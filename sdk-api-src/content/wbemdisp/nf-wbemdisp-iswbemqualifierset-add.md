---
UID: NF:wbemdisp.ISWbemQualifierSet.Add
title: ISWbemQualifierSet::Add
author: windows-sdk-content
description: The Add method of the SWbemQualifierSet object adds an SWbemQualifier object to the SWbemQualifierSet collection. If a qualifier with the same name already exists in the collection, it is replaced.
old-location: wmi\swbemqualifierset_add.htm
old-project: WmiSdk
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],ISWbemQualifierSet interface, Add method [Windows Management Instrumentation],SWbemQualifierSet object, ISWbemQualifierSet interface [Windows Management Instrumentation],Add method, ISWbemQualifierSet.Add, ISWbemQualifierSet::Add, SWbemQualifierSet object [Windows Management Instrumentation],Add method, SWbemQualifierSet.Add, _hmm_swbemqualifierset.add, wmi.swbemqualifierset_add
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
 - SWbemQualifierSet.Add
 - ISWbemQualifierSet.Add
 - ISWbemQualifierSet.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemQualifierSet::Add


## -description


The 
<b>Add</b> method of the 
<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a> object adds an 
<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a> object to the <b>SWbemQualifierSet</b> collection. If a qualifier with the same name already exists in the collection, it is replaced.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the new qualifier.


### -param varVal [in]

Required. Variant value of the new qualifier.


### -param bPropagatesToSubclass




### -param bPropagatesToInstance




### -param bIsOverridable




### -param iFlags [in, optional]

Reserved. The default value is 0.


### -param objWbemQualifier






#### - bPropagatesToSubclasses [in, optional]

Boolean value that indicates if this new qualifier is propagated to subclasses. The default value is <b>TRUE</b>.


#### - bPropagatesToInstances [in, optional]

Boolean value that indicates if this new qualifier is propagated to instances. The default value is <b>TRUE</b>.


#### - bOverridable [in, optional]

Boolean value that indicates if this qualifier can be overridden when propagated. The default value is <b>TRUE</b>.


## -returns



If successful, this method returns an <a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a> object that represents the new qualifier. Otherwise, a <b>null</b> object is returned.




## -see-also




<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a>



<a href="https://msdn.microsoft.com/7d386858-efd1-42e6-9176-9cb4bcfc77d0">SWbemQualifierSet.Remove</a>
 

 


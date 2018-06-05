---
UID: NE:wbemdisp.WbemQueryFlagEnum
title: WbemQueryFlagEnum
author: windows-sdk-content
description: Define the depth of enumeration or query, which determines how many objects are returned by a call.
old-location: wmi\wbemqueryflagenum.htm
old-project: WmiSdk
ms.assetid: 5da897fa-3dba-4360-bbbe-287da5717205
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WbemQueryFlagEnum, WbemQueryFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemqueryflagenum, wbemQueryFlagDeep, wbemQueryFlagPrototype, wbemQueryFlagShallow, wbemdisp/WbemQueryFlagEnum, wbemdisp/wbemQueryFlagDeep, wbemdisp/wbemQueryFlagPrototype, wbemdisp/wbemQueryFlagShallow, wmi.wbemqueryflagenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemQueryFlagEnum
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wbemdisp.h
api_name:
-	WbemQueryFlagEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WbemQueryFlagEnum enumeration


## -description


The 
<b>WbemQueryFlagEnum</b> constants define the depth of enumeration or query, which determines how many objects are returned by a call. These constants are used by 
<a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SWbemServices.SubclassesOf</a>, 
<a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">SWbemServices.InstancesOf</a>, 
<a href="https://msdn.microsoft.com/c17e5d4a-016f-42ae-bc11-e21a44772ce5">SWbemObject.Subclasses_</a>, and 
<a href="https://msdn.microsoft.com/30402d7d-f7cb-43b5-96b5-a8a76144e32d">SWbemObject.Instances_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemQueryFlagDeep

Forces recursive enumeration into all subclasses derived from the specified parent class. The parent class itself is not returned in the enumeration.


### -field wbemQueryFlagShallow

Forces the enumeration to include only immediate subclasses of the specified parent class.


### -field wbemQueryFlagPrototype

Used for prototyping. It stops the query from happening and instead returns an object that look like a typical result object.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 


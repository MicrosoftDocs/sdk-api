---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WbemFlagEnum enumeration


## -description


The <b>WbemFlagEnum</b> enumeration defines constants 
    that are used by <a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>, 
    <a href="https://msdn.microsoft.com/50c7f62b-dd83-4117-b10e-acee1690ce8c">SWbemServices.ExecQueryAsync</a>, 
    <a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SWbemServices.SubclassesOf</a>, and 
    <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">SWbemServices.InstancesOf</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this 
    library; script languages must use the value of the constant directly, unless they use the Windows Script Host 
    (WSH) XML file format. For more information, see 
    <a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemFlagReturnImmediately

Causes the call to return immediately.


### -field wbemFlagReturnWhenComplete

Causes this call to block until the call has completed.


### -field wbemFlagBidirectional

Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.


### -field wbemFlagForwardOnly

Causes a forward-only enumerator to be returned. Use this flag in combination with 
      <b>wbemFlagReturnImmediately</b> to request semisynchronous access. For more information, see 
      <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

You can only iterate (as in a VBScript For Each statement) through a forward-only enumerator one time. The 
      memory containing the instances is released by WMI so that the enumerator cannot be rewound. Therefore, the 
      <a href="https://msdn.microsoft.com/ad3d1265-a11e-4962-b1f3-60092d2f79ef">SWbemObjectSet.Count</a> method cannot be used since 
      it requires rewinding the enumerator.

Forward-only enumerators are generally much faster and use less 
      memory than conventional enumerators, but they do not allow calls to 
      <a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone</a>.


### -field wbemFlagNoErrorObject

This flag must not be set, and must be ignored on receipt.


### -field wbemFlagReturnErrorObject

Causes asynchronous calls to return an error object in the event of an error.


### -field wbemFlagSendStatus

Causes asynchronous calls to send status updates to the 
     <a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for your object 
     sink.


### -field wbemFlagDontSendStatus

Prevents asynchronous calls from sending status updates to the 
     <a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for your object 
     sink.


### -field wbemFlagEnsureLocatable


### -field wbemFlagDirectRead


### -field wbemFlagSendOnlySelected


### -field wbemFlagUseAmendedQualifiers

Causes WMI to return class amendment data along with the base class definition. For more information about 
     amended qualifiers, see 
     <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -field wbemFlagGetDefault


### -field wbemFlagSpawnInstance


### -field wbemFlagUseCurrentTime




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/3eae38e8-6a63-45c0-99b0-94e25ddbc5a8">Making a Semisynchronous Call with VBScript</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 


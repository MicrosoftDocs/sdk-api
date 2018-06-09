---
UID: NE:wbemdisp.WbemFlagEnum
title: WbemFlagEnum
author: windows-sdk-content
description: Defines constants that are used by SWbemServices.ExecQuery, SWbemServices.ExecQueryAsync, SWbemServices.SubclassesOf, and SWbemServices.InstancesOf.
old-location: wmi\wbemflagenum.htm
old-project: WmiSdk
ms.assetid: 51c54f70-9067-4523-9108-89af731b9d55
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: WbemFlagEnum, WbemFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemflagenum, wbemFlagBidirectional, wbemFlagDontSendStatus, wbemFlagForwardOnly, wbemFlagNoErrorObject, wbemFlagReturnErrorObject, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wbemdisp/WbemFlagEnum, wbemdisp/wbemFlagBidirectional, wbemdisp/wbemFlagDontSendStatus, wbemdisp/wbemFlagForwardOnly, wbemdisp/wbemFlagNoErrorObject, wbemdisp/wbemFlagReturnErrorObject, wbemdisp/wbemFlagReturnImmediately, wbemdisp/wbemFlagReturnWhenComplete, wbemdisp/wbemFlagSendStatus, wbemdisp/wbemFlagUseAmendedQualifiers, wmi.wbemflagenum
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
req.typenames: WbemFlagEnum
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemFlagEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 


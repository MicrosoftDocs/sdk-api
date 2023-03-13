---
UID: NE:wbemdisp.WbemFlagEnum
title: WbemFlagEnum (wbemdisp.h)
description: Defines constants that are used by SWbemServices.ExecQuery, SWbemServices.ExecQueryAsync, SWbemServices.SubclassesOf, and SWbemServices.InstancesOf.
helpviewer_keywords: ["WbemFlagEnum","WbemFlagEnum enumeration [Windows Management Instrumentation]","_hmm_wbemflagenum","wbemFlagBidirectional","wbemFlagDontSendStatus","wbemFlagForwardOnly","wbemFlagNoErrorObject","wbemFlagReturnErrorObject","wbemFlagReturnImmediately","wbemFlagReturnWhenComplete","wbemFlagSendStatus","wbemFlagUseAmendedQualifiers","wbemdisp/WbemFlagEnum","wbemdisp/wbemFlagBidirectional","wbemdisp/wbemFlagDontSendStatus","wbemdisp/wbemFlagForwardOnly","wbemdisp/wbemFlagNoErrorObject","wbemdisp/wbemFlagReturnErrorObject","wbemdisp/wbemFlagReturnImmediately","wbemdisp/wbemFlagReturnWhenComplete","wbemdisp/wbemFlagSendStatus","wbemdisp/wbemFlagUseAmendedQualifiers","wmi.wbemflagenum"]
old-location: wmi\wbemflagenum.htm
tech.root: wmi
ms.assetid: 51c54f70-9067-4523-9108-89af731b9d55
ms.date: 12/05/2018
ms.keywords: WbemFlagEnum, WbemFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemflagenum, wbemFlagBidirectional, wbemFlagDontSendStatus, wbemFlagForwardOnly, wbemFlagNoErrorObject, wbemFlagReturnErrorObject, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wbemdisp/WbemFlagEnum, wbemdisp/wbemFlagBidirectional, wbemdisp/wbemFlagDontSendStatus, wbemdisp/wbemFlagForwardOnly, wbemdisp/wbemFlagNoErrorObject, wbemdisp/wbemFlagReturnErrorObject, wbemdisp/wbemFlagReturnImmediately, wbemdisp/wbemFlagReturnWhenComplete, wbemdisp/wbemFlagSendStatus, wbemdisp/wbemFlagUseAmendedQualifiers, wmi.wbemflagenum
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WbemFlagEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemFlagEnum
 - wbemdisp/WbemFlagEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemFlagEnum
---

# WbemFlagEnum enumeration


## -description

The <b>WbemFlagEnum</b> enumeration defines constants 
    that are used by <a href="/windows/desktop/WmiSdk/swbemservices-execquery">SWbemServices.ExecQuery</a>, 
    <a href="/windows/desktop/WmiSdk/swbemservices-execqueryasync">SWbemServices.ExecQueryAsync</a>, 
    <a href="/windows/desktop/WmiSdk/swbemservices-subclassesof">SWbemServices.SubclassesOf</a>, and 
    <a href="/windows/desktop/WmiSdk/swbemservices-instancesof">SWbemServices.InstancesOf</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this 
    library; script languages must use the value of the constant directly, unless they use the Windows Script Host 
    (WSH) XML file format. For more information, see 
    <a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemFlagReturnImmediately:0x10

Causes the call to return immediately.

### -field wbemFlagReturnWhenComplete:0

Causes this call to block until the call has completed.

### -field wbemFlagBidirectional:0

Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.

### -field wbemFlagForwardOnly:0x20

Causes a forward-only enumerator to be returned. Use this flag in combination with 
      <b>wbemFlagReturnImmediately</b> to request semisynchronous access. For more information, see 
      <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

You can only iterate (as in a VBScript For Each statement) through a forward-only enumerator one time. The 
      memory containing the instances is released by WMI so that the enumerator cannot be rewound. Therefore, the 
      <a href="/windows/desktop/WmiSdk/swbemobjectset-count">SWbemObjectSet.Count</a> method cannot be used since 
      it requires rewinding the enumerator.

Forward-only enumerators are generally much faster and use less 
      memory than conventional enumerators, but they do not allow calls to 
      <a href="/windows/desktop/WmiSdk/swbemobject-clone-">SWbemObject.Clone</a>.

### -field wbemFlagNoErrorObject:0x40

This flag must not be set, and must be ignored on receipt.

### -field wbemFlagReturnErrorObject:0

Causes asynchronous calls to return an error object in the event of an error.

### -field wbemFlagSendStatus:0x80

Causes asynchronous calls to send status updates to the 
     <a href="/windows/desktop/WmiSdk/swbemsink-onprogress">SWbemSink.OnProgress</a> event handler for your object 
     sink.

### -field wbemFlagDontSendStatus:0

Prevents asynchronous calls from sending status updates to the 
     <a href="/windows/desktop/WmiSdk/swbemsink-onprogress">SWbemSink.OnProgress</a> event handler for your object 
     sink.

### -field wbemFlagEnsureLocatable:0x100

### -field wbemFlagDirectRead:0x200

### -field wbemFlagSendOnlySelected:0

### -field wbemFlagUseAmendedQualifiers:0x20000

Causes WMI to return class amendment data along with the base class definition. For more information about 
     amended qualifiers, see 
     <a href="/windows/desktop/WmiSdk/localizing-wmi-class-information">Localizing WMI Class Information</a>.

### -field wbemFlagGetDefault:0

### -field wbemFlagSpawnInstance:0x1

### -field wbemFlagUseCurrentTime:0x1

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/making-a-semisynchronous-call-with-vbscript">Making a Semisynchronous Call with VBScript</a>



<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>

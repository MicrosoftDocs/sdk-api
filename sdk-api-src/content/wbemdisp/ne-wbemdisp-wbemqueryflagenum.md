---
UID: NE:wbemdisp.WbemQueryFlagEnum
title: WbemQueryFlagEnum (wbemdisp.h)
description: Define the depth of enumeration or query, which determines how many objects are returned by a call.
helpviewer_keywords: ["WbemQueryFlagEnum","WbemQueryFlagEnum enumeration [Windows Management Instrumentation]","_hmm_wbemqueryflagenum","wbemQueryFlagDeep","wbemQueryFlagPrototype","wbemQueryFlagShallow","wbemdisp/WbemQueryFlagEnum","wbemdisp/wbemQueryFlagDeep","wbemdisp/wbemQueryFlagPrototype","wbemdisp/wbemQueryFlagShallow","wmi.wbemqueryflagenum"]
old-location: wmi\wbemqueryflagenum.htm
tech.root: wmi
ms.assetid: 5da897fa-3dba-4360-bbbe-287da5717205
ms.date: 12/05/2018
ms.keywords: WbemQueryFlagEnum, WbemQueryFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemqueryflagenum, wbemQueryFlagDeep, wbemQueryFlagPrototype, wbemQueryFlagShallow, wbemdisp/WbemQueryFlagEnum, wbemdisp/wbemQueryFlagDeep, wbemdisp/wbemQueryFlagPrototype, wbemdisp/wbemQueryFlagShallow, wmi.wbemqueryflagenum
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
req.typenames: WbemQueryFlagEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemQueryFlagEnum
 - wbemdisp/WbemQueryFlagEnum
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
 - WbemQueryFlagEnum
---

# WbemQueryFlagEnum enumeration


## -description

The 
<b>WbemQueryFlagEnum</b> constants define the depth of enumeration or query, which determines how many objects are returned by a call. These constants are used by 
<a href="/windows/desktop/WmiSdk/swbemservices-subclassesof">SWbemServices.SubclassesOf</a>, 
<a href="/windows/desktop/WmiSdk/swbemservices-instancesof">SWbemServices.InstancesOf</a>, 
<a href="/windows/desktop/WmiSdk/swbemobject-subclasses-">SWbemObject.Subclasses_</a>, and 
<a href="/windows/desktop/WmiSdk/swbemobject-instances-">SWbemObject.Instances_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemQueryFlagDeep:0

Forces recursive enumeration into all subclasses derived from the specified parent class. The parent class itself is not returned in the enumeration.

### -field wbemQueryFlagShallow:1

Forces the enumeration to include only immediate subclasses of the specified parent class.

### -field wbemQueryFlagPrototype:2

Used for prototyping. It stops the query from happening and instead returns an object that look like a typical result object.

## -see-also

<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>

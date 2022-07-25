---
UID: NE:wbemdisp.WbemChangeFlagEnum
title: WbemChangeFlagEnum (wbemdisp.h)
description: Define how a write operation to a class or an instance is carried out.
helpviewer_keywords: ["WbemChangeFlagEnum","WbemChangeFlagEnum enumeration [Windows Management Instrumentation]","_hmm_wbemchangeflagenum","wbemChangeFlagCreateOnly","wbemChangeFlagCreateOrUpdate","wbemChangeFlagStrongValidation","wbemChangeFlagUpdateCompatible","wbemChangeFlagUpdateForceMode","wbemChangeFlagUpdateOnly","wbemChangeFlagUpdateSafeMode","wbemdisp/WbemChangeFlagEnum","wbemdisp/wbemChangeFlagCreateOnly","wbemdisp/wbemChangeFlagCreateOrUpdate","wbemdisp/wbemChangeFlagStrongValidation","wbemdisp/wbemChangeFlagUpdateCompatible","wbemdisp/wbemChangeFlagUpdateForceMode","wbemdisp/wbemChangeFlagUpdateOnly","wbemdisp/wbemChangeFlagUpdateSafeMode","wmi.wbemchangeflagenum"]
old-location: wmi\wbemchangeflagenum.htm
tech.root: wmi
ms.assetid: 586a4a26-2044-4044-a90d-b45d05f6ce66
ms.date: 12/05/2018
ms.keywords: WbemChangeFlagEnum, WbemChangeFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemchangeflagenum, wbemChangeFlagCreateOnly, wbemChangeFlagCreateOrUpdate, wbemChangeFlagStrongValidation, wbemChangeFlagUpdateCompatible, wbemChangeFlagUpdateForceMode, wbemChangeFlagUpdateOnly, wbemChangeFlagUpdateSafeMode, wbemdisp/WbemChangeFlagEnum, wbemdisp/wbemChangeFlagCreateOnly, wbemdisp/wbemChangeFlagCreateOrUpdate, wbemdisp/wbemChangeFlagStrongValidation, wbemdisp/wbemChangeFlagUpdateCompatible, wbemdisp/wbemChangeFlagUpdateForceMode, wbemdisp/wbemChangeFlagUpdateOnly, wbemdisp/wbemChangeFlagUpdateSafeMode, wmi.wbemchangeflagenum
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
req.typenames: WbemChangeFlagEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemChangeFlagEnum
 - wbemdisp/WbemChangeFlagEnum
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
 - WbemChangeFlagEnum
---

# WbemChangeFlagEnum enumeration


## -description

The 
WbemChangeFlagEnum constants define how a write operation to a class or an instance is carried out. A write operation is executed by <a href="/windows/desktop/WmiSdk/swbemobject-put-">SWbemObject.Put_</a> or by <a href="/windows/desktop/WmiSdk/swbemservicesex-put">SWbemServicesEx.Put_</a>. These flags are used by 
<b>SWbemObject.Put_</b> and 
<a href="/windows/desktop/WmiSdk/swbemobject-putasync-">SWbemObject.PutAsync_</a>.

The WMI scripting type library, WbemDisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemChangeFlagCreateOrUpdate:0

Causes the class or instance to be created, if it does not exist, or overwritten if it already exists.

### -field wbemChangeFlagUpdateOnly:0x1

Causes the call to update. The class or instance must exist for the call to be successful.

### -field wbemChangeFlagCreateOnly:0x2

Used for creation only. The call will fail if the class or instance already exists.

### -field wbemChangeFlagUpdateCompatible:0

Allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to non-important qualifiers (for example, the <a href="/windows/desktop/WmiSdk/standard-qualifiers">Description</a> qualifier). If the class has instances, the update fails. This flag is used for compatibility with previous versions of WMI.

### -field wbemChangeFlagUpdateSafeMode:0x20

Allows updates of classes even if there are child classes as long as the change does not cause any conflicts with child classes. An example of an update this flag would allow would be to add a new property to the base class not previously mentioned in any of the child classes. If the class has instances, the update fails.

### -field wbemChangeFlagUpdateForceMode:0x40

Forces updates of classes when conflicting child classes exist.

An example of an update this flag forces would be if a class qualifier was defined in a child class, and the base class tried to add the same qualifier in conflict with the existing one. In the force mode, this conflict is resolved by deleting the qualifier in the child class. If the class has instances, the update fails.

Using the force mode to update a static class results in deletion of all instances of that class. Force update on provider classes does not delete instances of the class.

### -field wbemChangeFlagStrongValidation:0x80

<b>:  </b>Notifies the operating system to return a failure on put operations to any invalid system instances. Examples of such instances are event-related instances, such as filters, bindings, or providers. By default, if these instances are invalid, the put operation reports success but an error is reported in the log.

### -field wbemChangeFlagAdvisory:0x10000

## -see-also

<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>

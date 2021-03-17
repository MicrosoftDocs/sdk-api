---
UID: NF:wbemcli.IWbemClassObject.Delete
title: IWbemClassObject::Delete (wbemcli.h)
description: The IWbemClassObject::Delete method deletes the specified property from a CIM class definition and all of its qualifiers.
helpviewer_keywords: ["Delete","Delete method [Windows Management Instrumentation]","Delete method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","Delete method","IWbemClassObject.Delete","IWbemClassObject::Delete","_hmm_iwbemclassobject_delete","wbemcli/IWbemClassObject::Delete","wmi.iwbemclassobject_delete"]
old-location: wmi\iwbemclassobject_delete.htm
tech.root: wmi
ms.assetid: 01ccfad7-8529-4eb5-ae3a-cc1657022999
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Management Instrumentation], Delete method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],Delete method, IWbemClassObject.Delete, IWbemClassObject::Delete, _hmm_iwbemclassobject_delete, wbemcli/IWbemClassObject::Delete, wmi.iwbemclassobject_delete
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemClassObject::Delete
 - wbemcli/IWbemClassObject::Delete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.Delete
---

# IWbemClassObject::Delete


## -description

The 
<b>IWbemClassObject::Delete</b> method deletes the specified property from a CIM class definition and all of its qualifiers. Because instances cannot have contents that are different from the owning class, delete operations for properties are only possible on class definitions. If you invoke 
<b>Delete</b> on a property in an instance, the operation succeeds; however, rather than removing the value, it is simply reset to the default value for the class.

It is not possible to delete a property inherited from a parent class. However, if an override default value for a property inherited from a parent class was specified, it is possible to revert to the parent's default value by invoking this method. In this case, <b>WBEM_S_RESET_TO_DEFAULT</b> is returned.


<a href="/windows/desktop/WmiSdk/wmi-system-properties">System properties</a> cannot be deleted.

## -parameters

### -param wszName [in]

Property name to delete. This must point to a valid <b>LPCWSTR</b>. It is treated as read-only.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>
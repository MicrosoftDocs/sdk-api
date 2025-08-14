---
UID: NF:oleacc.CreateStdAccessibleObject
title: CreateStdAccessibleObject function (oleacc.h)
description: Creates an accessible object with the methods and properties of the specified type of system-provided user interface element.
helpviewer_keywords: ["CreateStdAccessibleObject","CreateStdAccessibleObject function [Windows Accessibility]","_msaa_CreateStdAccessibleObject","msaa.createstdaccessibleobject","oleacc/CreateStdAccessibleObject","winauto.createstdaccessibleobject"]
old-location: winauto\createstdaccessibleobject.htm
tech.root: WinAuto
ms.assetid: 50b6f391-98a4-4276-840f-028cc18e99ef
ms.date: 12/05/2018
ms.keywords: CreateStdAccessibleObject, CreateStdAccessibleObject function [Windows Accessibility], _msaa_CreateStdAccessibleObject, msaa.createstdaccessibleobject, oleacc/CreateStdAccessibleObject, winauto.createstdaccessibleobject
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - CreateStdAccessibleObject
 - oleacc/CreateStdAccessibleObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-oleacc-l1-1-2.dll
 - Oleacc.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - CreateStdAccessibleObject
---

# CreateStdAccessibleObject function


## -description

Creates an accessible object with the methods and properties of the specified type of system-provided user interface element.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Window handle of the system-provided user interface element (a control) for which an accessible object is created.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Object ID. This value is usually <a href="/windows/desktop/WinAuto/object-identifiers">OBJID_CLIENT</a>, but it may be another object identifier.

### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the requested interface. This value is one of the following: IID_IAccessible, IID_IDispatch, IID_IEnumVARIANT, or IID_IUnknown.

### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

## -remarks

Server applications call this function when they contain a custom UI object that is similar to a system-provided object. Server developers can call <b>CreateStdAccessibleObject</b> to override the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and properties as required to match their custom objects. Alternatively, server developers can use Dynamic Annotation to override specific properties without having to use difficult subclassing techniques that <b>CreateStdAccessibleObject</b> requires. Server developers should still use <b>CreateStdAccessibleObject</b> for structural changes, such as hiding a child element or creating a placeholder child element. This approach saves server developers the work of fully implementing all of the <b>IAccessible</b> properties and methods.

This function is similar to <a href="/windows/desktop/api/oleacc/nf-oleacc-createstdaccessibleproxya">CreateStdAccessibleProxy</a>, except that <b>CreateStdAccessibleProxy</b> allows you to specify the class name as a parameter whereas <b>CreateStdAccessibleObject</b> uses the class name associated with the <i>hwnd</i> parameter.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-createstdaccessibleproxya">CreateStdAccessibleProxy</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/shortcuts-for-exposing-custom-user-interface-elements">Shortcuts for Exposing Custom User Interface Elements</a>
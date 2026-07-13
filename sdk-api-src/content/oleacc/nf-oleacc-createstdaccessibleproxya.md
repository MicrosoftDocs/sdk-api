---
UID: NF:oleacc.CreateStdAccessibleProxyA
title: CreateStdAccessibleProxyA function (oleacc.h)
description: Creates an accessible object that has the properties and methods of the specified class of system-provided user interface element. (ANSI)
helpviewer_keywords: ["CreateStdAccessibleProxyA", "oleacc/CreateStdAccessibleProxyA"]
old-location: winauto\createstdaccessibleproxy.htm
tech.root: WinAuto
ms.assetid: 724b2a38-f7ca-4423-acd4-0871623d1201
ms.date: 12/05/2018
ms.keywords: CreateStdAccessibleProxy, CreateStdAccessibleProxy function [Windows Accessibility], CreateStdAccessibleProxyA, CreateStdAccessibleProxyW, _msaa_CreateStdAccessibleProxy, msaa.createstdaccessibleproxy, oleacc/CreateStdAccessibleProxy, oleacc/CreateStdAccessibleProxyA, oleacc/CreateStdAccessibleProxyW, winauto.createstdaccessibleproxy
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateStdAccessibleProxyW (Unicode) and CreateStdAccessibleProxyA (ANSI)
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
 - CreateStdAccessibleProxyA
 - oleacc/CreateStdAccessibleProxyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - CreateStdAccessibleProxy
 - CreateStdAccessibleProxyA
 - CreateStdAccessibleProxyW
---

# CreateStdAccessibleProxyA function


## -description

Creates an accessible object that has the properties and methods of the specified class of system-provided user interface element.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Window handle of the system-provided user interface element (a control) for which an accessible object is created.

### -param pClassName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

Pointer to a null-terminated string of the class name of a system-provided user interface element for which an accessible object is created. The window class name is one of the common controls (defined in Comctl32.dll), predefined controls (defined in User32.dll), or window elements.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Object ID. This value is usually <a href="/windows/desktop/WinAuto/object-identifiers">OBJID_CLIENT</a>, which is one of the object identifier constants, but it may be another object identifier.

### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the interface requested. This value is one of the following: IID_IAccessible, IID_IDispatch, IID_IEnumVARIANT, or IID_IUnknown.

### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

## -remarks

Server applications call this function when they contain a custom control that is similar to a system-provided control. Server applications can call <b>CreateStdAccessibleProxy</b> to override the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and properties as required to match their custom controls. Alternatively, server developers can use Dynamic Annotation to override specific properties without having to use difficult subclassing techniques that were required with <b>CreateStdAccessibleProxy</b>. Server developers should still use <b>CreateStdAccessibleProxy</b> for structural changes, such as hiding a child element or creating a placeholder child element. This approach saves server developers the work of fully implementing all of the <b>IAccessible</b> properties and methods.

This function is similar to <a href="/windows/desktop/api/oleacc/nf-oleacc-createstdaccessibleobject">CreateStdAccessibleObject</a>, except that <b>CreateStdAccessibleObject</b> always uses the class name associated with the <i>hwnd</i> whereas <b>CreateStdAccessibleProxy</b> allows you to specify the class name as a parameter.

Use <b>CreateStdAccessibleProxy</b> to create an accessible object for a user interface element that is superclassed. When a user interface element is superclassed, an application creates a custom control with a window class name different from the predefined control on which it is based. Because the class name associated with the <i>hwnd</i> parameter is the superclass window class name, specify the base class name (the system class name on which the superclassed control is based) in <i>pszClassName</i>.





> [!NOTE]
> The oleacc.h header defines CreateStdAccessibleProxy as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinAuto/appendix-a--supported-user-interface-elements-reference">Appendix A: Supported User Interface Elements Reference</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-createstdaccessibleobject">CreateStdAccessibleObject</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/shortcuts-for-exposing-custom-user-interface-elements">Shortcuts for Exposing Custom User Interface Elements</a>

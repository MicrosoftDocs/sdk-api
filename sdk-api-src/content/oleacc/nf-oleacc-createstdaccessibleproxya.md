---
UID: NF:oleacc.CreateStdAccessibleProxyA
title: CreateStdAccessibleProxyA function
author: windows-driver-content
description: Creates an accessible object that has the properties and methods of the specified class of system-provided user interface element.
old-location: winauto\createstdaccessibleproxy.htm
old-project: WinAuto
ms.assetid: 724b2a38-f7ca-4423-acd4-0871623d1201
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: CreateStdAccessibleProxy, CreateStdAccessibleProxy function [Windows Accessibility], CreateStdAccessibleProxyA, CreateStdAccessibleProxyW, _msaa_CreateStdAccessibleProxy, msaa.createstdaccessibleproxy, oleacc/CreateStdAccessibleProxy, oleacc/CreateStdAccessibleProxyA, oleacc/CreateStdAccessibleProxyW, winauto.createstdaccessibleproxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Oleacc.dll
api_name:
-	CreateStdAccessibleProxy
-	CreateStdAccessibleProxyA
-	CreateStdAccessibleProxyW
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# CreateStdAccessibleProxyA function


## -description


Creates an accessible object that has the properties and methods of the specified class of system-provided user interface element.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Window handle of the system-provided user interface element (a control) for which an accessible object is created.


### -param pClassName

TBD


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Object ID. This value is usually <a href="object_identifiers.htm">OBJID_CLIENT</a>, which is one of the object identifier constants, but it may be another object identifier.


### -param riid

TBD


### -param ppvObject [out]

Type: <b>void**</b>

Address of a pointer variable that receives the address of the specified interface.


#### - pszClassName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Pointer to a null-terminated string of the class name of a system-provided user interface element for which an accessible object is created. The window class name is one of the common controls (defined in Comctl32.dll), predefined controls (defined in User32.dll), or window elements.


#### - riidInterface [in]

Type: <b>REFIID</b>

Reference identifier of the interface requested. This value is one of the following: IID_IAccessible, IID_IDispatch, IID_IEnumVARIANT, or IID_IUnknown.


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.




## -remarks



Server applications call this function when they contain a custom control that is similar to a system-provided control. Server applications can call <b>CreateStdAccessibleProxy</b> to override the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and properties as required to match their custom controls. Alternatively, server developers can use Dynamic Annotation to override specific properties without having to use difficult subclassing techniques that were required with <b>CreateStdAccessibleProxy</b>. Server developers should still use <b>CreateStdAccessibleProxy</b> for structural changes, such as hiding a child element or creating a placeholder child element. This approach saves server developers the work of fully implementing all of the <b>IAccessible</b> properties and methods.

This function is similar to <a href="https://msdn.microsoft.com/50b6f391-98a4-4276-840f-028cc18e99ef">CreateStdAccessibleObject</a>, except that <b>CreateStdAccessibleObject</b> always uses the class name associated with the <i>hwnd</i> whereas <b>CreateStdAccessibleProxy</b> allows you to specify the class name as a parameter.

Use <b>CreateStdAccessibleProxy</b> to create an accessible object for a user interface element that is superclassed. When a user interface element is superclassed, an application creates a custom control with a window class name different from the predefined control on which it is based. Because the class name associated with the <i>hwnd</i> parameter is the superclass window class name, specify the base class name (the system class name on which the superclassed control is based) in <i>pszClassName</i>.




## -see-also




<a href="https://msdn.microsoft.com/5d0a81d8-5d36-4c33-bb8c-abcb8b00166e">Appendix A: Supported User Interface Elements Reference</a>



<a href="https://msdn.microsoft.com/50b6f391-98a4-4276-840f-028cc18e99ef">CreateStdAccessibleObject</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>



<a href="https://msdn.microsoft.com/024e1bfd-8cc2-4839-82ae-bd05dfec6449">Shortcuts for Exposing Custom User Interface Elements</a>
 

 


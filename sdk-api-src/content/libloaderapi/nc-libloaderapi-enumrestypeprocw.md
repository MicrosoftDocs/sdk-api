---
UID: NC:libloaderapi.ENUMRESTYPEPROCW
title: ENUMRESTYPEPROCW (libloaderapi.h)
author: windows-sdk-content
description: An application-defined callback function used with the EnumResourceTypes and EnumResourceTypesEx functions.
old-location: menurc\enumrestypeproc.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumrestypeproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumResTypeProc, EnumResTypeProc callback, EnumResTypeProc callback function [Menus and Other Resources], EnumResTypeProcA, EnumResTypeProcW, _win32_EnumResTypeProc, _win32_enumrestypeproc_cpp, libloaderapi/EnumResTypeProc, libloaderapi/EnumResTypeProcA, libloaderapi/EnumResTypeProcW, menurc.enumrestypeproc, winui._win32_enumrestypeproc
ms.topic: callback
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResTypeProcW (Unicode) and EnumResTypeProcA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - libloaderapi.h
api_name:
 - EnumResTypeProc
 - EnumResTypeProcA
 - EnumResTypeProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ENUMRESTYPEPROCW callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a> and <a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a> functions. It receives resource types. The <b>ENUMRESTYPEPROC</b> type defines a pointer to this callback function. <i>EnumResTypeProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resources for which the types are to be enumerated. If this parameter is <b>NULL</b>, the function enumerates the resource types in the module used to create the current process. 


### -param lpType


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined parameter passed to the <a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a> or <a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a> function. This parameter can be used in error checking. 


#### - lpszType [in]

Type: <b>LPTSTR</b>

The type of resource for which the type is being enumerated. 

Alternately, rather than a pointer, this parameter can be <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>(ID), where ID is the integer identifier of the given resource type. For standard resource types, see <a href="https://docs.microsoft.com/windows/desktop/menurc/resource-types">Resource Types</a>. For more information, see the Remarks section 

below.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a> or <a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a> function. 

If the callback function returns <b>FALSE</b>, then <a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a> or <a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a> will stop enumeration and return <b>FALSE</b>. On Windows XP and earlier the value obtained from <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will be <b>ERROR_SUCCESS</b>; starting with Windows Vista, the last error value will be <b>ERROR_RESOURCE_ENUM_USER_STOP</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/51a22bbf-e834-434e-8a2f-9d172d02b228">EnumResourceTypes</a>



<a href="https://msdn.microsoft.com/212ee064-b5d1-4309-9ee0-72340dd69328">EnumResourceTypesEx</a>



<a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 


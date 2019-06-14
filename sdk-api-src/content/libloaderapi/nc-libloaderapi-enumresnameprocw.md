---
UID: NC:libloaderapi.ENUMRESNAMEPROCW
title: ENUMRESNAMEPROCW (libloaderapi.h)
author: windows-sdk-content
description: An application-defined callback function used with the EnumResourceNames and EnumResourceNamesEx functions.
old-location: menurc\enumresnameproc.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\enumresnameproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumResNameProc, EnumResNameProc callback, EnumResNameProc callback function [Menus and Other Resources], EnumResNameProcA, EnumResNameProcW, _win32_EnumResNameProc, _win32_enumresnameproc_cpp, libloaderapi/EnumResNameProc, libloaderapi/EnumResNameProcA, libloaderapi/EnumResNameProcW, menurc.enumresnameproc, winui._win32_enumresnameproc
ms.topic: callback
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumResNameProcW (Unicode) and EnumResNameProcA (ANSI)
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
 - EnumResNameProc
 - EnumResNameProcA
 - EnumResNameProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ENUMRESNAMEPROCW callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/f64c766c-735f-43b7-84f9-339313c98ad3">EnumResourceNames</a> and <a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a> functions. It receives the type and name of a resource. The <b>ENUMRESNAMEPROC</b> type defines a pointer to this callback function. <i>EnumResNameProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resources that are being enumerated. If this parameter is <b>NULL</b>, the function enumerates the resource names in the module used to create the current process. 


### -param lpType


### -param lpName


### -param lParam [in]

Type: <b>LONG_PTR</b>

An application-defined parameter passed to the <a href="https://msdn.microsoft.com/f64c766c-735f-43b7-84f9-339313c98ad3">EnumResourceNames</a> or <a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a> function. This parameter can be used in error checking. 


#### - lpszName [in]

Type: <b>LPTSTR</b>

The name of a resource of the type being enumerated. Alternately, rather than a pointer, this parameter can be <code>MAKEINTRESOURCE(ID)</code>, where ID is the integer identifier of the resource. For more information, see the Remarks section below. 


#### - lpszType [in]

Type: <b>LPCTSTR</b>

The type of resource for which the name is being enumerated. Alternately, rather than a pointer, this parameter can be <code>MAKEINTRESOURCE(ID)</code>, where ID is an integer value representing a predefined resource type. For standard resource types, see <a href="winui._win32_Resource_Types">Resource Types</a>. For more information, see the Remarks section below. 


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration. 




## -remarks



If <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpszType</i>) is <b>TRUE</b>, then <i>lpszType</i> specifies the integer identifier of the given resource type. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource type. For example, the string "#258" represents the identifier 258.

Similarly, if <a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>(<i>lpszName</i>) is <b>TRUE</b>, then <i>lpszName</i> specifies the integer identifier of the given resource. Otherwise, it is a pointer to a null-terminated string. If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource.

An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/f64c766c-735f-43b7-84f9-339313c98ad3">EnumResourceNames</a> or <a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a> function.

If the callback function returns <b>FALSE</b>, then <a href="https://msdn.microsoft.com/f64c766c-735f-43b7-84f9-339313c98ad3">EnumResourceNames</a> or <a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a> will stop enumeration and return <b>FALSE</b>. On Windows XP and earlier the value obtained from <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will be <b>ERROR_SUCCESS</b>; starting with Windows Vista, the last error value will be <b>ERROR_RESOURCE_ENUM_USER_STOP</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f64c766c-735f-43b7-84f9-339313c98ad3">EnumResourceNames</a>



<a href="https://msdn.microsoft.com/d392c913-d71c-47fc-9b11-2688731d13e7">EnumResourceNamesEx</a>



<a href="https://msdn.microsoft.com/af7d1343-93b7-4e11-a299-3c2f19bb2e98">IS_INTRESOURCE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 


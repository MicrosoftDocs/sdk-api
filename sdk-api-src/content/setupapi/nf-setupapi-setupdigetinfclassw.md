---
UID: NF:setupapi.SetupDiGetINFClassW
title: SetupDiGetINFClassW function
author: windows-sdk-content
description: The SetupDiGetINFClass function returns the class of a specified device INF file.
old-location: devinst\setupdigetinfclass.htm
old-project: devinst
ms.assetid: 03e66c5b-9b76-4a40-8bd4-f640b689ce27
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SetupDiGetINFClass, SetupDiGetINFClass function [Device and Driver Installation], SetupDiGetINFClassA, SetupDiGetINFClassW, devinst.setupdigetinfclass, di-rtns_10b0e077-9fb8-4d84-9c74-10b896774d40.xml, setupapi/SetupDiGetINFClass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetINFClass
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiGetINFClassW function


## -description


The <b>SetupDiGetINFClass</b> function returns the class of a specified device INF file.


## -parameters




### -param InfName [in]

A pointer to a NULL-terminated string that supplies the name of a device INF file. This name can include a path. However, if just the file name is specified, the file is searched for in each directory that is listed in the <b>DevicePath</b> entry under the <b>HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion</b> subkey of the registry. The maximum length in characters, including a NULL terminator, of a NULL-terminated INF file name is MAX_PATH.


### -param ClassGuid [out]

A pointer to a variable of type GUID that receives the class GUID for the specified INF file. If the INF file does not specify a class name, the function returns a GUID_NULL structure. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550937">SetupDiClassGuidsFromName</a> to determine whether one or more classes with this name are already installed.


### -param ClassName [out]

A pointer to a buffer that receives a NULL-terminated string that contains the name of the class for the specified INF file. If the INF file does not specify a class name but does specify a GUID, this buffer receives the name that is retrieved by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff550947">SetupDiClassNameFromGuid</a>. However, if <b>SetupDiClassNameFromGuid</b> cannot retrieve a class name (for example, the class is not installed), it returns an empty string.


### -param ClassNameSize [in]

 The size, in characters, of the buffer that is pointed to by the <i>ClassName</i> parameter. The maximum length of a NULL-terminated class name, in characters, is MAX_CLASS_NAME_LEN.


### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the number of characters that are required to store the class name, including a terminating <b>NULL</b>. This pointer is optional and can be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Do not use this function with INF files for Windows 9x or Millennium Edition.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550909">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550937">SetupDiClassGuidsFromName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550947">SetupDiClassNameFromGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551053">SetupDiGetClassDescription</a>
 

 


---
UID: NF:setupapi.SetupDiGetClassDescriptionExA
title: SetupDiGetClassDescriptionExA function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetClassDescriptionEx function retrieves the description of a setup class installed on a local or remote computer.
old-location: devinst\setupdigetclassdescriptionex.htm
tech.root: devinst
ms.assetid: db3c6317-4f77-4ca6-96b8-4b26f6b04943
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiGetClassDescriptionEx, SetupDiGetClassDescriptionEx function [Device and Driver Installation], SetupDiGetClassDescriptionExA, SetupDiGetClassDescriptionExW, devinst.setupdigetclassdescriptionex, di-rtns_1e1110ab-59c3-42be-863a-396f329b114e.xml, setupapi/SetupDiGetClassDescriptionEx
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetClassDescriptionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetClassDescriptionExA function


## -description


The <b>SetupDiGetClassDescriptionEx</b> function retrieves the description of a setup class installed on a local or remote computer.


## -parameters




### -param ClassGuid [in]

A pointer to the GUID for the setup class whose description is to be retrieved.


### -param ClassDescription [out]

A pointer to a character buffer that receives the class description.


### -param ClassDescriptionSize [in]

The size, in characters, of the buffer that is pointed to by the <i>ClassDescription</i> parameter. The maximum length, in characters, of a NULL-terminated class description is LINE_LEN. For more information, see the following <b>Remarks</b> section. 


### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in characters, that is required to store the requested NULL-terminated class description. This pointer is optional and can be <b>NULL</b>.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that supplies the name of a remote computer on which the setup class resides. This pointer is optional and can be <b>NULL</b>. If the class is installed on a local computer, set the pointer to <b>NULL</b>. 


### -param Reserved

Reserved for system use. A caller of this function must set this parameter to <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If there is a friendly name in the registry key for the class, this routine returns the friendly name. Otherwise, this routine returns the class name.

<b>SetupDiGetClassDescriptionEx</b> does not enforce a restriction on the length of the class description that it can return. This function returns the required size for a NULL-terminated class description even if it is greater than LINE_LEN. However, LINE_LEN is the maximum length of a valid NULL-terminated class description. A caller should never need a buffer that is larger than LINE_LEN. 




## -see-also




<a href="https://msdn.microsoft.com/a01b1f8f-55af-4053-8c31-9329ef36f2ce">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/32c6c548-79f8-41be-ad9a-5456972a16eb">SetupDiBuildClassInfoListEx</a>



<a href="https://msdn.microsoft.com/3f624882-9ccc-4be1-92aa-8bba9f0022ea">SetupDiGetDeviceInfoListDetail</a>



<a href="https://msdn.microsoft.com/03e66c5b-9b76-4a40-8bd4-f640b689ce27">SetupDiGetINFClass</a>
 

 


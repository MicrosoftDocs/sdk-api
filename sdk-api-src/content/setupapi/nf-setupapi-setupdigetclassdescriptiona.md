---
UID: NF:setupapi.SetupDiGetClassDescriptionA
title: SetupDiGetClassDescriptionA function
author: windows-sdk-content
description: The SetupDiGetClassDescription function retrieves the class description associated with the specified setup class GUID.
old-location: devinst\setupdigetclassdescription.htm
tech.root: devinst
ms.assetid: a9757c77-f873-4f75-be80-c4bd1d327299
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupDiGetClassDescription, SetupDiGetClassDescription function [Device and Driver Installation], SetupDiGetClassDescriptionA, SetupDiGetClassDescriptionW, devinst.setupdigetclassdescription, di-rtns_90458b4a-959d-4344-ae06-c88cbdbbfbdf.xml, setupapi/SetupDiGetClassDescription
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SetupDiGetClassDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetClassDescriptionA function


## -description


The <b>SetupDiGetClassDescription</b> function retrieves the class description associated with the specified setup class GUID.


## -parameters




### -param ClassGuid [in]

The GUID of the setup class whose description is to be retrieved.


### -param ClassDescription [out]

A pointer to a character buffer that receives the class description.


### -param ClassDescriptionSize [in]

The size, in characters, of the <i>ClassDescription</i> buffer.


### -param RequiredSize [out, optional]

A pointer to variable of type DWORD that receives the size, in characters, that is required to store the class description (including a NULL terminator). <i>RequiredSize</i> is always less than LINE_LEN. This parameter is optional and can be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <b>SetupDiGetClassDescriptionEx</b> to retrieve the description of a setup class installed on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/a01b1f8f-55af-4053-8c31-9329ef36f2ce">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/db3c6317-4f77-4ca6-96b8-4b26f6b04943">SetupDiGetClassDescriptionEx</a>



<a href="https://msdn.microsoft.com/03e66c5b-9b76-4a40-8bd4-f640b689ce27">SetupDiGetINFClass</a>
 

 


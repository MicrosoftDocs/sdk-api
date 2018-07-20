---
UID: NF:setupapi.SetupDiClassNameFromGuidExW
title: SetupDiClassNameFromGuidExW function
author: windows-sdk-content
description: The SetupDiClassNameFromGuidEx function retrieves the class name associated with a class GUID. The class can be installed on a local or remote computer.
old-location: devinst\setupdiclassnamefromguidex.htm
old-project: devinst
ms.assetid: 0d576df1-e259-4025-8ef0-a520f5680fa0
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: SetupDiClassNameFromGuidEx, SetupDiClassNameFromGuidEx function [Device and Driver Installation], SetupDiClassNameFromGuidExA, SetupDiClassNameFromGuidExW, devinst.setupdiclassnamefromguidex, di-rtns_69da61fd-b042-4b1b-92a4-d40418f18794.xml, setupapi/SetupDiClassNameFromGuidEx
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
 - SetupDiClassNameFromGuidEx
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiClassNameFromGuidExW function


## -description


The <b>SetupDiClassNameFromGuidEx</b> function retrieves the class name associated with a class GUID. The class can be installed on a local or remote computer.


## -parameters




### -param ClassGuid [in]

The class GUID of the class name to retrieve.


### -param ClassName [out]

A pointer to a string buffer that receives the NULL-terminated name of the class for the specified GUID.


### -param ClassNameSize [in]

The size, in characters, of the <i>ClassName</i> buffer.


### -param RequiredSize [out, optional]

The number of characters required to store the class name (including a terminating null). <i>RequiredSize</i> is always less than MAX_CLASS_NAME_LEN.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system on which the class is installed. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the local system name is used.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550941">SetupDiClassGuidsFromNameEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550947">SetupDiClassNameFromGuid</a>
 

 


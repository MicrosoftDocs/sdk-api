---
UID: NF:setupapi.SetupDiClassGuidsFromNameExA
title: SetupDiClassGuidsFromNameExA function
author: windows-sdk-content
description: The SetupDiClassGuidsFromNameEx function retrieves the GUIDs associated with the specified class name. This resulting list contains the classes currently installed on a local or remote computer.
old-location: devinst\setupdiclassguidsfromnameex.htm
tech.root: devinst
ms.assetid: 5a692ed0-2e3a-464e-934e-2fe98d9c217b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetupDiClassGuidsFromNameEx, SetupDiClassGuidsFromNameEx function [Device and Driver Installation], SetupDiClassGuidsFromNameExA, SetupDiClassGuidsFromNameExW, devinst.setupdiclassguidsfromnameex, di-rtns_de553347-9025-4477-8d83-9d1bdac1ceff.xml, setupapi/SetupDiClassGuidsFromNameEx
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
 - SetupDiClassGuidsFromNameEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiClassGuidsFromNameExA function


## -description


The <b>SetupDiClassGuidsFromNameEx</b> function retrieves the GUIDs associated with the specified class name. This resulting list contains the classes currently installed on a local or remote computer.


## -parameters




### -param ClassName [in]

The name of the class for which to retrieve the class GUIDs.


### -param ClassGuidList [out]

A pointer to an array to receive the list of GUIDs associated with the specified class name.


### -param ClassGuidListSize [in]

The number of GUIDs in the <i>ClassGuidList</i> array.


### -param RequiredSize [out]

A pointer to a variable that receives the number of GUIDs associated with the class name. If this number is greater than the size of the <i>ClassGuidList</i> buffer, the number indicates how large the array must be in order to store all the GUIDs.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system from which to retrieve the GUIDs. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the local system name is used.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Class names are not guaranteed to be unique; only GUIDs are unique. Therefore, one class name can return more than one GUID.




## -see-also




<a href="https://msdn.microsoft.com/54516c6f-ec78-47ea-93f5-a4c7cde5a601">SetupDiClassGuidsFromName</a>



<a href="https://msdn.microsoft.com/0d576df1-e259-4025-8ef0-a520f5680fa0">SetupDiClassNameFromGuidEx</a>
 

 

